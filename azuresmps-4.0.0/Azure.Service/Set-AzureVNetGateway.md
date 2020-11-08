---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046414"
---
# Set-AzureVNetGateway

## SYNOPSIS
Azure 가상 네트워크에 대 한 VPN 게이트웨이를 사용 하거나 사용 하지 않도록 설정 합니다.

## 구문과

### 연결 (기본값)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### 끊고
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Set-AzureVNetGateway** Cmdlet은 Azure 가상 네트워크에 대 한 VPN (가상 사설망) 게이트웨이를 사용 하거나 사용 하지 않도록 설정 합니다.
가상 네트워크 게이트웨이는 가상 네트워크에 연결 하기 위한 VPN 끝점입니다.
*연결* 또는 *연결 끊기* 매개 변수를 지정 하 여 온-프레미스 로컬 네트워크 사이트와 가상 네트워크 간의 VPN 연결을 사용 하거나 사용 하지 않도록 설정 합니다.

## 예제의

### 예제 1: 가상 네트워크에 가상 네트워크 게이트웨이 사용
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

이 명령을 사용 하면 ContosoProdNet 이라는 Azure 가상 네트워크와 ContosoBranchOffice 라는 로컬 네트워크 사이트의 VPN 장치 간에 가상 네트워크 게이트웨이를 사용할 수 있습니다.

### 예제 2: 가상 네트워크에 대 한 가상 네트워크 게이트웨이 사용 안 함
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

이 명령은 ContosoProdNet 이라는 Azure 가상 네트워크와 ContosoBranchOffice 라는 로컬 네트워크 사이트의 VPN 장치 간 가상 네트워크 게이트웨이를 사용 하지 않도록 설정 합니다.

## 변수

### -연결
이 cmdlet이 가상 네트워크와 로컬 네트워크 사이트 간의 VPN 연결을 사용할 수 있음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -연결 끊기
이 cmdlet이 가상 네트워크와 로컬 네트워크 사이트 간 VPN 연결을 사용 하지 않도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
이 cmdlet이 VPN 연결을 사용 하거나 사용 하지 않도록 설정 하는 온-프레미스 로컬 네트워크 사이트의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -VNetName
이 cmdlet이 VPN 연결을 사용 하거나 사용 하지 않도록 설정 하는 가상 네트워크를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[새-AzureVNetGateway](./New-AzureVNetGateway.md)

[-AzureVNetGateway 제거](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[크기 조정-AzureVNetGateway](./Resize-AzureVNetGateway.md)


