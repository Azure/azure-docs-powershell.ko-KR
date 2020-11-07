---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703953"
---
# <span data-ttu-id="40ee5-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="40ee5-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="40ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="40ee5-103">사이트 복구 복제 정책 연결 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ee5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40ee5-104">SYNTAX</span></span>

### <span data-ttu-id="40ee5-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="40ee5-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40ee5-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="40ee5-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ee5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="40ee5-107">DESCRIPTION</span></span>
<span data-ttu-id="40ee5-108">**AzureRmSiteRecoveryPolicyAssociationJob** cmdlet은 복제 정책을 Azure Site Recovery 보호 컨테이너와 연결 하는 연결 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="40ee5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="40ee5-109">EXAMPLES</span></span>

## <span data-ttu-id="40ee5-110">변수</span><span class="sxs-lookup"><span data-stu-id="40ee5-110">PARAMETERS</span></span>

### <span data-ttu-id="40ee5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ee5-111">-DefaultProfile</span></span>
<span data-ttu-id="40ee5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40ee5-113">-정책</span><span class="sxs-lookup"><span data-stu-id="40ee5-113">-Policy</span></span>
<span data-ttu-id="40ee5-114">사이트 복구 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-114">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="40ee5-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="40ee5-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="40ee5-116">보호 프로필 설정을 적용할 기본 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="40ee5-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="40ee5-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="40ee5-118">보호 프로필 설정을 적용할 복구 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="40ee5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ee5-119">CommonParameters</span></span>
<span data-ttu-id="40ee5-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ee5-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ee5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ee5-122">입력</span><span class="sxs-lookup"><span data-stu-id="40ee5-122">INPUTS</span></span>

### <span data-ttu-id="40ee5-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="40ee5-123">ASRPolicy</span></span>
<span data-ttu-id="40ee5-124">' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40ee5-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="40ee5-125">출력</span><span class="sxs-lookup"><span data-stu-id="40ee5-125">OUTPUTS</span></span>

### <span data-ttu-id="40ee5-126">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="40ee5-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="40ee5-127">상속자</span><span class="sxs-lookup"><span data-stu-id="40ee5-127">NOTES</span></span>

## <span data-ttu-id="40ee5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40ee5-128">RELATED LINKS</span></span>

