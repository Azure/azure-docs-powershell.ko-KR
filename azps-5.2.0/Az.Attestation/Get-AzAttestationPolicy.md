---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 64a74902d1a5b10ed36c635b58910246634e68b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353342"
---
# Get-AzAttestationPolicy

## SYNOPSIS
Azure Attestation의 테넌트에서 정책을 얻습니다.

## 구문

### NameParameterSet
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DefaultProviderParameterSet
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Get-AzAttestationPolicy cmdlet은 Azure Attestation의 테넌트에서 정책을 얻습니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

Tee 형식 *SgxEnclave에* 대한 Attestation Provider *pshtest에* 대한 정책을 얻습니다.

### 예제 2
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

Tee 형식 *SgxEnclave에* 대한 *영국* 남부 위치의 Attestation 기본 공급자에 대한 정책을 얻습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProvider
기본 등록 공급자에 대한 요청으로 지정합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
기본 등록 공급자의 위치를 지정합니다.

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
테넌트의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 테넌트에 대한 설명 정책을 얻습니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
등록 공급자의 리소스 그룹 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
등록 공급자의 ResourceID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tee
신뢰할 수 있는 실행 환경의 유형을 지정합니다.
SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave의 네 가지 유형의 환경을 지원합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Attestation.Models.PSPolicy

## 참고 사항

## 관련 링크
