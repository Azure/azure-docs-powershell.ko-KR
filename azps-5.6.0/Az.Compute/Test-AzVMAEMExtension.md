---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010779"
---
# Test-AzVMAEMExtension

## SYNOPSIS
AEM 확장의 구성을 검사합니다.

## 구문

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Test-AzVMAEMExtension** cmdlet은 AEM(Azure Enhanced Monitoring) 확장의 구성을 검사합니다.
AEM 확장은 성능 데이터를 수집합니다.
이 cmdlet은 성능 데이터를 사용할 수 있는지 여부를 검사합니다.

## 예제

### 예제 1: AEM 확장 구성 확인
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

이 명령은 contoso-server라는 가상 머신에 대한 AEM 확장 구성을 검사합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -OSType
운영 체제 디스크의 운영 체제 유형을 지정합니다.
운영 체제 디스크에 형식이 없는 경우 이 매개 변수를 지정해야 합니다.
이 매개 변수에 대해 허용되는 값은 Windows 및 Linux입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet에서 검사하는 가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorageCheck
이 cmdlet이 저장소 구성 검사를 건너뛰고 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
가상 머신의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 AEM 확장을 테스트합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WaitTimeInMinutes
저장소 구성 검사에 대한 시간 시간(분)을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult

## 참고 사항

## 관련 링크

[Get-AzVMAEMExtension](./Get-AzVMAEMExtension.md)

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Set-AzVMAEMExtension](./Set-AzVMAEMExtension.md)


