---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876584"
---
# Set-AzLoadBalancer

## SYNOPSIS
부하 분산 장치에 대 한 목표 상태를 설정 합니다.

## 구문과

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzLoadBalancer** Cmdlet은 Azure 부하 분산 장치에 대 한 목표 상태를 설정 합니다.

## 예제의

### 예제 1: 부하 분산 장치 수정
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

첫 번째 명령은 NRPLB 이라는 부하 분산 장치를 가져온 다음이를 $slb 변수에 저장 합니다.

두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 로드 균형 조정기를 Add-AzLoadBalancerInboundNatRuleConfig에 전달 하 여 NewRule 이라는 인바운드 NAT 규칙을 추가 합니다.

세 번째 명령은 부하 분산 장치 구성을 업데이트 하 고 저장 하는 부하 분산을 **설정-AzLoadBalancer** 에 전달 합니다.

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

### -LoadBalancer
부하 분산 장치를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 목표 상태를 설정 합니다.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSLoadBalancer
' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. 네트워크. PSLoadBalancer

## 상속자

## 관련 링크

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[새로운 AzLoadBalancer](./New-AzLoadBalancer.md)

[제거-AzLoadBalancer](./Remove-AzLoadBalancer.md)


