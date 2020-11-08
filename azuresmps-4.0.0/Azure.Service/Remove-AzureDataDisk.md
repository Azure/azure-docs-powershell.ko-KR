---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046166"
---
# Remove-AzureDataDisk

## SYNOPSIS
Azure 가상 머신에서 데이터 디스크를 제거 합니다.

## 구문과

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**제거-AzureDataDisk** Cmdlet은 Azure 가상 머신에서 데이터 디스크를 제거 합니다.
기본적으로이 cmdlet은 저장소 계정에서 데이터 디스크 blob을 제거 하지 않습니다.

## 예제의

### 예제 1: 데이터 디스크 제거
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

이 명령은 VirtualMachine07 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.
현재 cmdlet은 LUN 0이 있는 데이터 디스크를 제거 합니다.

### 예제 2: 데이터 디스크 및 가상 하드 디스크 파일 제거
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

이 명령은 ContosoService 이라는 서비스에서 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.
명령이 가상 컴퓨터를 현재 cmdlet에 전달 합니다.
현재 cmdlet은 LUN 0이 있는 데이터 디스크를 제거 합니다.
명령에는 *Deletevhd* 매개 변수가 포함 됩니다.
따라서 기본 가상 하드 디스크도 삭제 됩니다.
이 명령은 **업데이트-add-azurevm** cmdlet을 사용 하 여 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.

## 변수

### -DeleteVHD
이 cmdlet이 blob 저장소에서 데이터 디스크와 VHD (가상 하드 디스크)를 제거 함을 나타냅니다.

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

### -LUN
가상 컴퓨터의 데이터 드라이브에 대 한 LUN (논리 단위 번호)을 지정 합니다.
유효한 값은 0 ~ 15입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -VM
데이터 디스크에 연결 된 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

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

## 상속자

## 관련 링크

[-AzureDataDisk 추가](./Add-AzureDataDisk.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[Set AzureDataDisk](./Set-AzureDataDisk.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


