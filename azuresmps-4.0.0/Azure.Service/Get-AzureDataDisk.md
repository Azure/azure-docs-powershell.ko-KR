---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045651"
---
# Get-AzureDataDisk

## SYNOPSIS
Azure 데이터 디스크를 가져옵니다.

## 구문과

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-AzureDataDisk** Cmdlet은 Azure 가상 컴퓨터의 데이터 디스크를 나타내는 개체를 가져옵니다.
특정 데이터 디스크 개체를 가져오려면 디스크의 LUN (논리 단위 번호)을 지정 합니다.

## 예제의

### 예제 1: 가상 컴퓨터용 모든 데이터 디스크 가져오기
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

이 명령은 VirtualMachine07 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.
현재 cmdlet은이 가상 컴퓨터에 대 한 모든 데이터 디스크를 가져옵니다.

### 예제 2: vituralvirtual machinevirtual 용 특정 데이터 디스크 가져오기
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

이 명령은 ContosoService 이라는 서비스에서 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.
명령이 가상 컴퓨터를 현재 cmdlet에 전달 합니다.
현재 cmdlet은 LUN 2가 있는 데이터 디스크를 가져옵니다.

## 변수

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

### -Lun
가상 컴퓨터의 데이터 드라이브에 대 한 LUN을 지정 합니다.
유효한 값은 0 ~ 15입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
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
이 cmdlet에서 데이터 디스크를 가져오는 가상 컴퓨터 개체를 지정 합니다.
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

[다운로드-Add-azurevm](./Get-AzureVM.md)

[-AzureDataDisk 제거](./Remove-AzureDataDisk.md)

[Set AzureDataDisk](./Set-AzureDataDisk.md)


