---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 950c5c8e2007568add1aba1122356de670884c07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534608"
---
# <span data-ttu-id="54832-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="54832-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="54832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54832-102">SYNOPSIS</span></span>
<span data-ttu-id="54832-103">정책을 보호 컨테이너에 연결 하 여 Azure Site Recovery 보호 컨테이너 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54832-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54832-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54832-104">SYNTAX</span></span>

### <span data-ttu-id="54832-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="54832-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54832-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="54832-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54832-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54832-107">DESCRIPTION</span></span>
<span data-ttu-id="54832-108">**AzureRmSiteRecoveryProtectionContainerMapping** cmdlet은 정책을 보호 컨테이너에 연결 하 여 Azure Site Recovery 보호 컨테이너 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54832-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="54832-109">예제의</span><span class="sxs-lookup"><span data-stu-id="54832-109">EXAMPLES</span></span>

## <span data-ttu-id="54832-110">변수</span><span class="sxs-lookup"><span data-stu-id="54832-110">PARAMETERS</span></span>

### <span data-ttu-id="54832-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54832-111">-DefaultProfile</span></span>
<span data-ttu-id="54832-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54832-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54832-113">-이름</span><span class="sxs-lookup"><span data-stu-id="54832-113">-Name</span></span>
<span data-ttu-id="54832-114">보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54832-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54832-115">-정책</span><span class="sxs-lookup"><span data-stu-id="54832-115">-Policy</span></span>
<span data-ttu-id="54832-116">Azure Site Recovery 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54832-116">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="54832-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="54832-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="54832-118">주 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54832-118">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="54832-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="54832-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="54832-120">복구 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54832-120">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="54832-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54832-121">CommonParameters</span></span>
<span data-ttu-id="54832-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54832-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54832-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54832-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54832-124">입력</span><span class="sxs-lookup"><span data-stu-id="54832-124">INPUTS</span></span>

### <span data-ttu-id="54832-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="54832-125">ASRPolicy</span></span>
<span data-ttu-id="54832-126">' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54832-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="54832-127">출력</span><span class="sxs-lookup"><span data-stu-id="54832-127">OUTPUTS</span></span>

### <span data-ttu-id="54832-128">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="54832-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54832-129">상속자</span><span class="sxs-lookup"><span data-stu-id="54832-129">NOTES</span></span>

## <span data-ttu-id="54832-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54832-130">RELATED LINKS</span></span>

[<span data-ttu-id="54832-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="54832-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="54832-132">제거-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="54832-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
