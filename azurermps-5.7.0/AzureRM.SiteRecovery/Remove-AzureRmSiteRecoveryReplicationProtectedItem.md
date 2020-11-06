---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534591"
---
# <span data-ttu-id="d5c03-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5c03-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="d5c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c03-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c03-103">Azure Site Recovery 복제 보호 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5c03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5c03-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c03-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5c03-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c03-106">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet은 Azure Site Recovery 복제 보호 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="d5c03-107">이 작업을 수행 하면 보호 된 항목에 대 한 복제가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="d5c03-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d5c03-108">EXAMPLES</span></span>

## <span data-ttu-id="d5c03-109">변수</span><span class="sxs-lookup"><span data-stu-id="d5c03-109">PARAMETERS</span></span>

### <span data-ttu-id="d5c03-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c03-110">-DefaultProfile</span></span>
<span data-ttu-id="d5c03-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5c03-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d5c03-112">-Force</span></span>
<span data-ttu-id="d5c03-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5c03-114">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5c03-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d5c03-115">복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-115">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c03-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d5c03-116">-WaitForCompletion</span></span>
<span data-ttu-id="d5c03-117">Cmdlet이 작업이 완료 될 때까지 대기 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="d5c03-118">-확인</span><span class="sxs-lookup"><span data-stu-id="d5c03-118">-Confirm</span></span>
<span data-ttu-id="d5c03-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c03-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c03-120">-WhatIf</span></span>
<span data-ttu-id="d5c03-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d5c03-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c03-123">CommonParameters</span></span>
<span data-ttu-id="d5c03-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c03-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c03-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c03-126">입력</span><span class="sxs-lookup"><span data-stu-id="d5c03-126">INPUTS</span></span>

### <span data-ttu-id="d5c03-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5c03-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="d5c03-128">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5c03-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="d5c03-129">출력</span><span class="sxs-lookup"><span data-stu-id="d5c03-129">OUTPUTS</span></span>

### <span data-ttu-id="d5c03-130">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="d5c03-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d5c03-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d5c03-131">NOTES</span></span>

## <span data-ttu-id="d5c03-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5c03-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5c03-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5c03-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="d5c03-134">새로운 AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5c03-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="d5c03-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5c03-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
