---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045819"
---
# Set-AzureServiceProject

## SYNOPSIS
현재 서비스의 기본 위치, 구독, 슬롯 및 저장소 계정을 설정 합니다.

## 구문과

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Set-AzureServiceProject** cmdlet은 현재 서비스에 대 한 배포 위치, 슬롯, 저장소 계정 및 구독을 설정 합니다.
이러한 값은 서비스를 클라우드에 게시할 때마다 사용 됩니다.

## 예제의

### 예제 1: 기본 설정
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

서비스의 배포 위치를 북쪽 중부 US 지역으로 설정 합니다.
배포 슬롯을 프로덕션으로 설정 합니다. MyStorageAccount에 대 한 서비스 정의를 준비 하는 데 사용할 저장소 계정을 설정 합니다.
서비스를 mySubscription에 호스팅할 구독을 설정 합니다.
서비스를 클라우드에 게시할 때마다 해당 서비스가 북미 중앙 미국 지역의 데이터 센터에서 호스팅되므로 배포 슬롯이 업데이트 되며 지정 된 구독 및 저장소 계정이 사용 됩니다.

## 변수

### -위치
서비스를 호스팅할 영역입니다.
서비스를 클라우드에 게시할 때마다이 값이 사용 됩니다.
가능한 값은 어디에서 든 아시아, 어디서 나 유럽, 어디서 나 미국, 동쪽 미국, 북부 중앙 미국, 동유럽, 남 중앙 미국, 동남 아시아, 서유럽, 서쪽 미국입니다.

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

### -PassThru
이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

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

### -슬롯
서비스를 호스트할 슬롯 (제작 또는 준비)입니다.
서비스를 클라우드에 게시할 때마다이 값이 사용 됩니다.
사용할 수 있는 값은 프로덕션, 준비입니다.

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

### -저장소
클라우드에 서비스 패키지를 업로드할 때 사용할 저장소 계정입니다.
저장소 계정이 없는 경우 서비스를 클라우드에 게시할 때 생성 됩니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자
* 노드 개발자, php-개발자, python-개발자

## 관련 링크

[새-AzureServiceProject](./New-AzureServiceProject.md)

[게시-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


