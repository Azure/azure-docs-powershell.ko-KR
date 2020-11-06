---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 869b22c881652680be31c541c6d70d95a45be43d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529115"
---
# <span data-ttu-id="4904a-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4904a-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="4904a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4904a-102">SYNOPSIS</span></span>
<span data-ttu-id="4904a-103">Azure Site Recovery 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4904a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4904a-104">SYNTAX</span></span>

### <span data-ttu-id="4904a-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="4904a-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4904a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4904a-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4904a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4904a-107">DESCRIPTION</span></span>
<span data-ttu-id="4904a-108">**AzureRmSiteRecoveryProtectionContainerMapping** cmdlet은 자격 증명 모음의 정책 매핑에 대 한 보호 컨테이너에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="4904a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4904a-109">EXAMPLES</span></span>

## <span data-ttu-id="4904a-110">변수</span><span class="sxs-lookup"><span data-stu-id="4904a-110">PARAMETERS</span></span>

### <span data-ttu-id="4904a-111">-이름</span><span class="sxs-lookup"><span data-stu-id="4904a-111">-Name</span></span>
<span data-ttu-id="4904a-112">보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4904a-113">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4904a-113">-ProtectionContainer</span></span>
<span data-ttu-id="4904a-114">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-114">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4904a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4904a-115">-DefaultProfile</span></span>
<span data-ttu-id="4904a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4904a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4904a-117">CommonParameters</span></span>
<span data-ttu-id="4904a-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4904a-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4904a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4904a-120">입력</span><span class="sxs-lookup"><span data-stu-id="4904a-120">INPUTS</span></span>

### <span data-ttu-id="4904a-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4904a-121">ASRProtectionContainer</span></span>
<span data-ttu-id="4904a-122">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4904a-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="4904a-123">출력</span><span class="sxs-lookup"><span data-stu-id="4904a-123">OUTPUTS</span></span>

### <span data-ttu-id="4904a-124">ASRProtectionContainerMapping, SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]], system.webserver ' 1 [[Microsoft Azure.])</span><span class="sxs-lookup"><span data-stu-id="4904a-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4904a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="4904a-125">NOTES</span></span>

## <span data-ttu-id="4904a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4904a-126">RELATED LINKS</span></span>

[<span data-ttu-id="4904a-127">새로운 AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4904a-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="4904a-128">제거-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4904a-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
