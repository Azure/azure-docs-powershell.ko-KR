---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046057"
---
# Set-AzureEndpoint

## SYNOPSIS
가상 컴퓨터에 할당 된 끝점을 수정 합니다.

## 구문과

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Set azureendpoint** Cmdlet은 Azure 가상 컴퓨터에 할당 된 끝점을 수정 합니다.
부하 분산 되지 않은 끝점에 대 한 변경 내용을 지정할 수 있습니다.

## 예제의

### 예제 1: 끝점을 수정 하 여 포트에서 수신
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

이 명령은 **get-help** cmdlet을 사용 하 여 VirtualMachine01 이라는 가상 컴퓨터의 구성을 검색 합니다.
이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.
이 cmdlet은 포트 443에서 수신 하도록 Web 이라는 끝점을 수정 합니다.
이 명령은 가상 컴퓨터 개체를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.

## 변수

### -ACL
이 cmdlet이 끝점에 적용 하는 ACL (액세스 제어 목록) 구성 개체를 지정 합니다.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectServerReturn
이 cmdlet이 직접 서버 반환을 사용할 수 있는지 여부를 지정 합니다.
사용할 $True를 지정 하거나 사용 하지 않을 $False.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
끝점에 대 한 TCP 유휴 시간 제한 기간 (분)을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -InternalLoadBalancerName
내부 부하 분산의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerDistribution
부하 분산 장치 배포 알고리즘을 지정 합니다.
유효한 값은 다음과 같습니다. 

- sourceIP.
두 가지 튜플 선호도: 원본 IP, 대상 IP 
- sourceIPProtocol.
세 가지 튜플 선호도: 원본 IP, 대상 IP, 프로토콜 
- 않아야.
5 개의 튜플 선호도: 원본 IP, 원본 포트, 대상 IP, 대상 포트, 프로토콜 

기본값은 없음입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPort
이 끝점에서 사용 하는 로컬, 개인 포트를 지정 합니다.
가상 컴퓨터 내의 응용 프로그램은이 끝점에 대 한 서비스 입력 요청에 대해이 포트에서 수신 대기 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
끝점의 이름을 지정 합니다.

```yaml
Type: String
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

### -프로토콜
끝점의 프로토콜을 지정 합니다.
유효한 값은 다음과 같습니다. 

- net.tcp 
- udp

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicPort
끝점에서 사용 하는 공용 포트를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualIPName
Azure가 끝점에 연결 하는 가상 IP 주소의 이름을 지정 합니다.
서비스에 여러 개의 가상 Ip가 있을 수 있습니다.
가상 Ip를 만들려면 **Add-AzureVirtualIP** cmdlet을 사용 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
끝점이 속한 가상 컴퓨터를 지정 합니다.

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

### System. 개체

## 상속자

## 관련 링크

[추가-AzureEndpoint](./Add-AzureEndpoint.md)

[추가-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[-AzureEndpoint 제거](./Remove-AzureEndpoint.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


