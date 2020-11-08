---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046353"
---
# Get-AzureEffectiveRouteTable

## SYNOPSIS
가상 컴퓨터에 적용 된 경로를 가져옵니다.

## 구문과

### IaaSGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SlotGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureEffectiveRouteTable** cmdlet은 가상 컴퓨터에 적용 된 경로를 가져옵니다.
이 작업을 완료 하는 데 몇 초 정도 걸릴 수 있습니다.

## 예제의

### 예제 1: 가상 컴퓨터를 적용 한 유효한 경로 가져오기
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.
현재 cmdlet은 해당 가상 컴퓨터에 적용 된 경로를 가져옵니다.

## 변수

### -NetworkInterfaceName
이 cmdlet이 유효한 경로를 가져오는 네트워크 어댑터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstanceName
이 cmdlet이 유효한 경로를 가져오는 PaaS 역할의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
클라우드 서비스의 이름을 지정 합니다.
이 cmdlet이 유효한 경로를 가져오는 PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
PaaS 슬롯을 지정 합니다.
이 cmdlet이 유효한 경로를 가져오는 PaaS 역할에는이 매개 변수에서 지정 하는 슬롯이 있습니다.
유효한 값은 다음과 같습니다. 

- 프로덕션용
- 대기 

기본값은 실제 값입니다.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
이 cmdlet이 유효한 경로를 가져오는 가상 컴퓨터 개체를 지정 합니다.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure, EffectiveRouteTable, WindowsAzure에 대 한 system.webserver<. a. a. m a. 네트워크>

## 상속자

## 관련 링크

[Get-AzureRouteTable](./Get-AzureRouteTable.md)

[새로운 AzureRouteTable](./New-AzureRouteTable.md)

[제거-AzureRouteTable](./Remove-AzureRouteTable.md)

[제거-AzureSubnetRouteTable](./Remove-AzureSubnetRouteTable.md)

[Set-AzureSubnetRouteTable](./Set-AzureSubnetRouteTable.md)


