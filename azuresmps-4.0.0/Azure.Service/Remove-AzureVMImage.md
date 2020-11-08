---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046454"
---
# Remove-AzureVMImage

## SYNOPSIS
이미지 리포지토리에서 운영 체제 이미지를 제거 합니다.

## 구문과

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureVMImage** cmdlet은 이미지 리포지토리에서 운영 체제 이미지를 제거 합니다.
기본적으로이 cmdlet은 저장소 계정에서 연결 된 실제 이미지 blob을 삭제 하지 않습니다.
연결 된 VHD (가상 하드 드라이브)를 삭제 하려면 **Deletevhd** 매개 변수를 사용 합니다.

## 예제의

### 예제 1: 이미지 리포지토리에서 이미지 제거
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

이 명령은 이미지 리포지토리에서 Image001 이라는 이미지를 제거 합니다.

### 예제 2: 이미지 리포지토리에서 이미지를 제거 하 고 VHD도
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

이 명령은 이미지 리포지토리에서 Image001 이라는 이미지를 제거 하 고 저장소 계정에서 실제 VHD 이미지도 삭제 합니다.

### 예제 3: 구독 컨텍스트를 설정한 다음 모든 이미지 제거
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

이 명령은 구독 컨텍스트를 설정한 다음 해당 레이블에 이름 Beta가 포함 된 이미지 리포지토리에서 모든 이미지를 제거 합니다.

## 변수

### -DeleteVHD
이 cmdlet이 저장소 계정에서 실제 VHD 이미지 blob을 삭제 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
이미지 리포지토리에서 제거할 운영 체제 또는 가상 컴퓨터 이미지를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[저장-AzureVMImage](./Save-AzureVMImage.md)

[업데이트-AzureVMImage](./Update-AzureVMImage.md)


