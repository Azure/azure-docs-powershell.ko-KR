---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9e33f3e956f7d1fee0d93eebf5e14fa0df460303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013691"
---
# Set-AzVMDiagnosticsExtension

## SYNOPSIS
가상 머신에서 Azure 진단 확장을 구성합니다.

## 구문

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure 진단 확장을 구성합니다.

## 예제

### 예제 1: 진단 구성 파일에 지정된 저장소 계정을 사용하여 진단 사용
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

이 명령은 진단 구성 파일을 사용하여 진단을 사용하도록 설정합니다.
파일 diagnostics_publicconfig.xml 진단 데이터가 전송될 저장소 계정의 이름을 포함하여 진단 확장에 대한 공용 XML 구성이 포함되어 있습니다.
진단 저장소 계정은 가상 머신과 동일한 구독에 있어야 합니다.

### 예제 2: 저장소 계정 이름을 사용하여 진단 사용
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

이 명령은 저장소 계정 이름을 사용하여 진단을 사용하도록 설정합니다.
진단 구성에서 저장소 계정 이름을 지정하지 않는 경우 또는 구성 파일에 지정된 진단 저장소 계정 이름을 다시 정의하려는 경우 *StorageAccountName* 매개 변수를 사용합니다.
진단 저장소 계정은 가상 머신과 동일한 구독에 있어야 합니다.

### 예제 3: 저장소 계정 이름 및 키를 사용하여 진단 사용
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

이 명령은 저장소 계정 이름 및 키를 사용하여 진단을 사용하도록 설정합니다.
진단 저장소 계정이 가상 머신과 다른 구독에 있는 경우 해당 이름 및 키를 명시적으로 지정하여 진단 데이터를 해당 저장소 계정에 보낼 수 있습니다.

## 매개 변수

### -AutoUpgradeMinorVersion
이 cmdlet을 통해 Azure 게스트 에이전트가 확장을 최신 부 버전으로 자동으로 업데이트할 수 있는지 여부를 나타냅니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DiagnosticsConfigurationPath
구성 파일의 경로를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
가상 머신의 위치를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
확장의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다. 작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

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

### -StorageAccountEndpoint
저장소 계정 엔드포인트를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
저장소 계정 키를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
저장소 계정 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Azure Storage 컨텍스트를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
이 가상 머신에 사용할 확장 버전을 지정합니다.
버전을 얻게 Get-AzVMExtensionImage *Type* 매개 변수에 대한 Microsoft.Compute 매개 변수 및 VMAccessAgent 값을 사용하여 Get-AzVMExtensionImage cmdlet을 *실행합니다.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
이 cmdlet이 작동하는 가상 머신의 이름을 지정합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

### System.Boolean

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzVMDiagnosticsExtension](./Get-AzVMDiagnosticsExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)

[Remove-AzVMDiagnosticsExtension](./Remove-AzVMDiagnosticsExtension.md)


