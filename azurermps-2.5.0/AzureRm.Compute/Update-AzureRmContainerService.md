---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883102"
---
# Update-AzureRmContainerService

## SYNOPSIS
컨테이너 서비스의 상태를 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**업데이트 AzureRmContainerService** cmdlet은 서비스의 로컬 인스턴스와 일치 하도록 컨테이너 서비스의 상태를 업데이트 합니다.

## 예제의

### 예제 1: 컨테이너 서비스 업데이트
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

이 명령은 Get-AzureRmContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 Remove-AzureRmContainerServiceAgentPoolProfile cmdlet에 해당 개체를 전달 합니다.

**제거-AzureRmContainerServiceAgentPoolProfile** 는 AgentPool01 이라는 프로필을 제거 합니다.
명령이 결과를 Add-AzureRmContainerServiceAgentPoolProfile cmdlet에 전달 합니다.

**추가-AzureRmContainerServiceAgentPoolProfile** 이름이 AgentPool01이 고 지정 된 속성이 있는 프로필을 추가 합니다.
명령이 결과를 현재 cmdlet에 전달 합니다.

현재 cmdlet은이 명령에 대 한 변경 내용을 반영 하도록 컨테이너 서비스를 업데이트 합니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerService
변경 내용이 포함 된 로컬 **ContainerService** 개체를 지정 합니다.

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 업데이트 하는 컨테이너 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 업데이트 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### ContainerService
' ContainerService ' 매개 변수는 파이프라인에서 ' ContainerService ' 형식의 값을 허용 합니다.

## 출력

### PSContainerService의. m a.

## 상속자

## 관련 링크

[추가-AzureRmContainerServiceAgentPoolProfile](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[Get-AzureRmContainerService](./Get-AzureRmContainerService.md)

[새로운 AzureRmContainerService](./New-AzureRmContainerService.md)

[제거-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[제거-AzureRmContainerServiceAgentPoolProfile](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


