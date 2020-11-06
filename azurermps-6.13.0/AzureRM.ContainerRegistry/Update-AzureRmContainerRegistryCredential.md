---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536683"
---
# Update-AzureRmContainerRegistryCredential

## SYNOPSIS
컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NameResourceGroupParameterSet (기본값)
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RegistryObjectParameterSet
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Update-AzureRmContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.

## 예제의

### 예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 다시 생성
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.
\` \` 로그인 자격 증명을 다시 생성 하기 위해 관리 사용자에 게 컨테이너 레지스트리 myregistry을 사용 하도록 설정 해야 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
컨테이너 레지스트리 이름입니다.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordName
다시 생성할 암호의 이름입니다.
허용 되는 값: password, password2.

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -레지스트리
컨테이너 레지스트리 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
컨테이너 레지스트리 리소스 id

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### ContainerRegistry. PSContainerRegistry
매개 변수: Registry (ByValue)

### System. 문자열

## 출력

### ContainerRegistry. PSContainerRegistryCredential

## 상속자

## 관련 링크

[새로운 AzureRmContainerRegistry](New-AzureRmContainerRegistry.md)

[업데이트-AzureRmContainerRegistry](Update-AzureRmContainerRegistry.md)

[Get-AzureRmContainerRegistryCredential](Get-AzureRmContainerRegistryCredential.md)

