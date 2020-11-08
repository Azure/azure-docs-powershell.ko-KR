---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042642"
---
# <span data-ttu-id="b3b38-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b3b38-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b3b38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b38-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b38-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 네트워크 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="b3b38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3b38-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3b38-105">DESCRIPTION</span></span>
<span data-ttu-id="b3b38-106">**AzRecoveryServicesAsrNetworkMapping** cmdlet은 지정 된 ASR 네트워크 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="b3b38-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3b38-107">EXAMPLES</span></span>

### <span data-ttu-id="b3b38-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3b38-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="b3b38-109">지정 된 ASR 네트워크 매핑 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b3b38-110">변수</span><span class="sxs-lookup"><span data-stu-id="b3b38-110">PARAMETERS</span></span>

### <span data-ttu-id="b3b38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b38-111">-DefaultProfile</span></span>
<span data-ttu-id="b3b38-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b38-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b38-113">-InputObject</span></span>
<span data-ttu-id="b3b38-114">Cmdlet에 대 한 입력 개체: 삭제할 ASR 네트워크 매핑에 해당 하는 ASR 네트워크 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b38-115">-확인</span><span class="sxs-lookup"><span data-stu-id="b3b38-115">-Confirm</span></span>
<span data-ttu-id="b3b38-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b38-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b38-117">-WhatIf</span></span>
<span data-ttu-id="b3b38-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3b38-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b38-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b38-120">CommonParameters</span></span>
<span data-ttu-id="b3b38-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3b38-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b38-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3b38-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b38-123">입력</span><span class="sxs-lookup"><span data-stu-id="b3b38-123">INPUTS</span></span>

### <span data-ttu-id="b3b38-124">SiteRecovery. r m g Networkmapping 매핑</span><span class="sxs-lookup"><span data-stu-id="b3b38-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="b3b38-125">출력</span><span class="sxs-lookup"><span data-stu-id="b3b38-125">OUTPUTS</span></span>

### <span data-ttu-id="b3b38-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="b3b38-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b3b38-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b3b38-127">NOTES</span></span>

## <span data-ttu-id="b3b38-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3b38-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3b38-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b3b38-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="b3b38-130">새로운 AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b3b38-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
