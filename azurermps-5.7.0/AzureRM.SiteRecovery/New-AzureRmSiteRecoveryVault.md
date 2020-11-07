---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 0b70fe2636ae0bc460afd05f9428708c0ff4963b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703963"
---
# <span data-ttu-id="fef48-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fef48-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="fef48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef48-102">SYNOPSIS</span></span>
<span data-ttu-id="fef48-103">사이트 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fef48-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef48-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fef48-105">DESCRIPTION</span></span>
<span data-ttu-id="fef48-106">**AzureRmSiteRecoveryVault** Cmdlet은 Azure Site Recovery 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="fef48-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fef48-107">EXAMPLES</span></span>

## <span data-ttu-id="fef48-108">변수</span><span class="sxs-lookup"><span data-stu-id="fef48-108">PARAMETERS</span></span>

### <span data-ttu-id="fef48-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef48-109">-DefaultProfile</span></span>
<span data-ttu-id="fef48-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef48-111">-위치</span><span class="sxs-lookup"><span data-stu-id="fef48-111">-Location</span></span>
<span data-ttu-id="fef48-112">지리적 위치 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-112">Specifies the geographical location name.</span></span>

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

### <span data-ttu-id="fef48-113">-이름</span><span class="sxs-lookup"><span data-stu-id="fef48-113">-Name</span></span>
<span data-ttu-id="fef48-114">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="fef48-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef48-115">-ResourceGroupName</span></span>
<span data-ttu-id="fef48-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fef48-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef48-117">CommonParameters</span></span>
<span data-ttu-id="fef48-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef48-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef48-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef48-120">입력</span><span class="sxs-lookup"><span data-stu-id="fef48-120">INPUTS</span></span>

### <span data-ttu-id="fef48-121">않아야</span><span class="sxs-lookup"><span data-stu-id="fef48-121">None</span></span>
<span data-ttu-id="fef48-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fef48-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fef48-123">출력</span><span class="sxs-lookup"><span data-stu-id="fef48-123">OUTPUTS</span></span>

## <span data-ttu-id="fef48-124">상속자</span><span class="sxs-lookup"><span data-stu-id="fef48-124">NOTES</span></span>

## <span data-ttu-id="fef48-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fef48-125">RELATED LINKS</span></span>

[<span data-ttu-id="fef48-126">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fef48-126">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="fef48-127">제거-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fef48-127">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
