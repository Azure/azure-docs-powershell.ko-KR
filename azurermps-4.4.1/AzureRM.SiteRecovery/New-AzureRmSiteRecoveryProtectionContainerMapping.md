---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532923"
---
# <span data-ttu-id="2356d-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2356d-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="2356d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2356d-102">SYNOPSIS</span></span>
<span data-ttu-id="2356d-103">정책을 보호 컨테이너에 연결 하 여 Azure Site Recovery 보호 컨테이너 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2356d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2356d-104">SYNTAX</span></span>

### <span data-ttu-id="2356d-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="2356d-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2356d-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="2356d-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2356d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2356d-107">DESCRIPTION</span></span>
<span data-ttu-id="2356d-108">**AzureRmSiteRecoveryProtectionContainerMapping** cmdlet은 정책을 보호 컨테이너에 연결 하 여 Azure Site Recovery 보호 컨테이너 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="2356d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2356d-109">EXAMPLES</span></span>

## <span data-ttu-id="2356d-110">변수</span><span class="sxs-lookup"><span data-stu-id="2356d-110">PARAMETERS</span></span>

### <span data-ttu-id="2356d-111">-이름</span><span class="sxs-lookup"><span data-stu-id="2356d-111">-Name</span></span>
<span data-ttu-id="2356d-112">보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2356d-113">-정책</span><span class="sxs-lookup"><span data-stu-id="2356d-113">-Policy</span></span>
<span data-ttu-id="2356d-114">Azure Site Recovery 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-114">Specifies the Azure Site Recovery Policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2356d-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2356d-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="2356d-116">주 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-116">Specifies the primary Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2356d-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2356d-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="2356d-118">복구 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-118">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2356d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2356d-119">-DefaultProfile</span></span>
<span data-ttu-id="2356d-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2356d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2356d-121">CommonParameters</span></span>
<span data-ttu-id="2356d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2356d-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2356d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2356d-124">입력</span><span class="sxs-lookup"><span data-stu-id="2356d-124">INPUTS</span></span>

### <span data-ttu-id="2356d-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="2356d-125">ASRPolicy</span></span>
<span data-ttu-id="2356d-126">' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2356d-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="2356d-127">출력</span><span class="sxs-lookup"><span data-stu-id="2356d-127">OUTPUTS</span></span>

### <span data-ttu-id="2356d-128">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="2356d-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2356d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="2356d-129">NOTES</span></span>

## <span data-ttu-id="2356d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2356d-130">RELATED LINKS</span></span>

[<span data-ttu-id="2356d-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2356d-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="2356d-132">제거-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2356d-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
