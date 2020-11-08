---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046322"
---
# Get-AzureRemoteAppOperationResult

## SYNOPSIS
Azure RemoteApp 작업의 결과를 검색 합니다.

## 구문과

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureRemoteAppOperationResult** cmdlet은 장기 실행 Azure RemoteApp 작업의 결과를 검색 합니다.
Azure RemoteApp은 서비스에서 처리 해야 하며 즉시 반환할 수 없는 많은 작업에 장기 실행 작업을 사용 합니다.
추적 Id를 반환 하는 cmdlet의 예로는 **업데이트-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** 등이 있습니다.

## 예제의

### 예제 1: 추적 ID를 사용 하 여 작업 결과 가져오기
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

이 명령은 Azure RemoteApp 작업에서 반환 된 추적 ID를 저장 합니다.
추적 ID는 다음 명령에서 **Get-AzureRemoteAppOperationResult** 에 전달 됩니다.

## 변수

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -TrackingId
작업의 추적 ID를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[연결 해제-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Set-AzureRemoteAppWorkspace](./Set-AzureRemoteAppWorkspace.md)

[업데이트-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


