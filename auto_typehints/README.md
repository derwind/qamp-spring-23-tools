# auto_typehints

This is a tool to assist with type hinting in [qiskit-terra](https://github.com/Qiskit/qiskit-terra).

## Usage

1. Clone qiskit-terra
2. Place `auto_typehints.py` in the root of qiskit-terra.
3. Execute the following command:

```sh
python auto_typehints.py
```

## Typical use

The typical use of this tool is to support type hinting for `quantum_info`, which is used as follows:

```sh
python -auto_typehints.py --qiskit-root qiskit --inplace quantum_info
```

If limited to `qiskit.quantum_info.states.statevector` only, use the following:

```sh
python auto_typehints.py -qiskit-root qiskit --only statevector.py quantum_info
```

Furthermore, if you want to write the result to another file instead of overwriting it, you can give the file a suffix as follows:

```sh
python auto_typehints.py -qiskit-root qiskit --only statevector.py --suffix .hinted quantum_info
```
