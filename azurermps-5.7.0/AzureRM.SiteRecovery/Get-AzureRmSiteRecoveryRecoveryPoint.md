---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534635"
---
# <span data-ttu-id="10a84-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10a84-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="10a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a84-102">SYNOPSIS</span></span>
<span data-ttu-id="10a84-103">복제 보호 항목에 대 한 사용 가능한 복구 지점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10a84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10a84-104">SYNTAX</span></span>

### <span data-ttu-id="10a84-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="10a84-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10a84-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="10a84-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10a84-107">설명은</span><span class="sxs-lookup"><span data-stu-id="10a84-107">DESCRIPTION</span></span>
<span data-ttu-id="10a84-108">**AzureRmSiteRecoveryRecoveryPoint** cmdlet은 복제 보호 항목에 대해 사용 가능한 복구 지점 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="10a84-109">예제의</span><span class="sxs-lookup"><span data-stu-id="10a84-109">EXAMPLES</span></span>

## <span data-ttu-id="10a84-110">변수</span><span class="sxs-lookup"><span data-stu-id="10a84-110">PARAMETERS</span></span>

### <span data-ttu-id="10a84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a84-111">-DefaultProfile</span></span>
<span data-ttu-id="10a84-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a84-113">-이름</span><span class="sxs-lookup"><span data-stu-id="10a84-113">-Name</span></span>
<span data-ttu-id="10a84-114">이 cmdlet이 가져오는 복구 지점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a84-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="10a84-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="10a84-116">Azure Site Recovery 복제 보호 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

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

### <span data-ttu-id="10a84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a84-117">CommonParameters</span></span>
<span data-ttu-id="10a84-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a84-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a84-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a84-120">입력</span><span class="sxs-lookup"><span data-stu-id="10a84-120">INPUTS</span></span>

### <span data-ttu-id="10a84-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="10a84-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="10a84-122">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a84-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="10a84-123">출력</span><span class="sxs-lookup"><span data-stu-id="10a84-123">OUTPUTS</span></span>

### <span data-ttu-id="10a84-124">ASRRecoveryPoint, SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]], system.webserver ' 1 [[Microsoft Azure.])</span><span class="sxs-lookup"><span data-stu-id="10a84-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="10a84-125">상속자</span><span class="sxs-lookup"><span data-stu-id="10a84-125">NOTES</span></span>

## <span data-ttu-id="10a84-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10a84-126">RELATED LINKS</span></span>

[<span data-ttu-id="10a84-127">편집-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10a84-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="10a84-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10a84-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="10a84-129">새로운 AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10a84-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="10a84-130">제거-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10a84-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="10a84-131">업데이트-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10a84-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
