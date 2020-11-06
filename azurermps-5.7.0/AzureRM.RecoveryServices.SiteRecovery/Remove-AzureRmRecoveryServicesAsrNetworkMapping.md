---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a51be31c510d7e428ced0c9ce5ab73a80ab28f75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526644"
---
# <span data-ttu-id="b470f-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b470f-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b470f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b470f-102">SYNOPSIS</span></span>
<span data-ttu-id="b470f-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 네트워크 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b470f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b470f-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b470f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b470f-105">DESCRIPTION</span></span>
<span data-ttu-id="b470f-106">**AzureRmRecoveryServicesAsrNetworkMapping** cmdlet은 지정 된 ASR 네트워크 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="b470f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b470f-107">EXAMPLES</span></span>

### <span data-ttu-id="b470f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b470f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="b470f-109">지정 된 ASR 네트워크 매핑 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b470f-110">변수</span><span class="sxs-lookup"><span data-stu-id="b470f-110">PARAMETERS</span></span>

### <span data-ttu-id="b470f-111">-확인</span><span class="sxs-lookup"><span data-stu-id="b470f-111">-Confirm</span></span>
<span data-ttu-id="b470f-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b470f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b470f-113">-DefaultProfile</span></span>
<span data-ttu-id="b470f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b470f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b470f-115">-InputObject</span></span>
<span data-ttu-id="b470f-116">Cmdlet에 대 한 입력 개체: 삭제할 ASR 네트워크 매핑에 해당 하는 ASR 네트워크 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-116">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b470f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b470f-117">-WhatIf</span></span>
<span data-ttu-id="b470f-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b470f-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b470f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b470f-120">CommonParameters</span></span>
<span data-ttu-id="b470f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b470f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b470f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b470f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b470f-123">입력</span><span class="sxs-lookup"><span data-stu-id="b470f-123">INPUTS</span></span>

### <span data-ttu-id="b470f-124">SiteRecovery. r m g Networkmapping 매핑</span><span class="sxs-lookup"><span data-stu-id="b470f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="b470f-125">출력</span><span class="sxs-lookup"><span data-stu-id="b470f-125">OUTPUTS</span></span>

### <span data-ttu-id="b470f-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="b470f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b470f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b470f-127">NOTES</span></span>

## <span data-ttu-id="b470f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b470f-128">RELATED LINKS</span></span>

[<span data-ttu-id="b470f-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b470f-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="b470f-130">새로운 AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b470f-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
