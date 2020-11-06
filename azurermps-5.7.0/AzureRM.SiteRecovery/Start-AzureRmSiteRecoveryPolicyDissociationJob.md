---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicydissociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: eb12462b85c4a12416f41f899ebc9b2c46cca465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533612"
---
# <span data-ttu-id="20dbc-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="20dbc-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="20dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="20dbc-103">사이트 복구 보호 컨테이너와 연결 된 복제 정책에서 dissociation 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20dbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20dbc-104">SYNTAX</span></span>

### <span data-ttu-id="20dbc-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="20dbc-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20dbc-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="20dbc-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20dbc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="20dbc-108">**AzureRmSiteRecoveryPolicyDissociationJob** Cmdlet은 Azure Site Recovery 보호 컨테이너와 연결 된 복제 정책에서 dissociation 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="20dbc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20dbc-109">EXAMPLES</span></span>

## <span data-ttu-id="20dbc-110">변수</span><span class="sxs-lookup"><span data-stu-id="20dbc-110">PARAMETERS</span></span>

### <span data-ttu-id="20dbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20dbc-111">-DefaultProfile</span></span>
<span data-ttu-id="20dbc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20dbc-113">-정책</span><span class="sxs-lookup"><span data-stu-id="20dbc-113">-Policy</span></span>
<span data-ttu-id="20dbc-114">Azure Site Recovery 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-114">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20dbc-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20dbc-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="20dbc-116">주 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-116">Specifies a primary protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dbc-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20dbc-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="20dbc-118">복구 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-118">Specifies a recovery protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dbc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dbc-119">CommonParameters</span></span>
<span data-ttu-id="20dbc-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dbc-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20dbc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dbc-122">입력</span><span class="sxs-lookup"><span data-stu-id="20dbc-122">INPUTS</span></span>

### <span data-ttu-id="20dbc-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="20dbc-123">ASRPolicy</span></span>
<span data-ttu-id="20dbc-124">' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20dbc-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="20dbc-125">출력</span><span class="sxs-lookup"><span data-stu-id="20dbc-125">OUTPUTS</span></span>

### <span data-ttu-id="20dbc-126">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="20dbc-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="20dbc-127">상속자</span><span class="sxs-lookup"><span data-stu-id="20dbc-127">NOTES</span></span>

## <span data-ttu-id="20dbc-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20dbc-128">RELATED LINKS</span></span>

