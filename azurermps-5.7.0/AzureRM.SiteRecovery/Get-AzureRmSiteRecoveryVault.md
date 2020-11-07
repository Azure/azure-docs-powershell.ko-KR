---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703972"
---
# <span data-ttu-id="21d46-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="21d46-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="21d46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21d46-102">SYNOPSIS</span></span>
<span data-ttu-id="21d46-103">현재 구독에서 사이트 복구 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21d46-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="21d46-105">DESCRIPTION</span></span>
<span data-ttu-id="21d46-106">**AzureRmSiteRecoveryVault** cmdlet은 현재 구독에서 Azure site recovery 자격 증명 모음 또는 특정 사이트 복구 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="21d46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="21d46-107">EXAMPLES</span></span>

## <span data-ttu-id="21d46-108">변수</span><span class="sxs-lookup"><span data-stu-id="21d46-108">PARAMETERS</span></span>

### <span data-ttu-id="21d46-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d46-109">-DefaultProfile</span></span>
<span data-ttu-id="21d46-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21d46-111">-이름</span><span class="sxs-lookup"><span data-stu-id="21d46-111">-Name</span></span>
<span data-ttu-id="21d46-112">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-112">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d46-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d46-113">-ResourceGroupName</span></span>
<span data-ttu-id="21d46-114">복구 서비스 개체를 가져올 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d46-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d46-115">CommonParameters</span></span>
<span data-ttu-id="21d46-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d46-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d46-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d46-118">입력</span><span class="sxs-lookup"><span data-stu-id="21d46-118">INPUTS</span></span>

### <span data-ttu-id="21d46-119">않아야</span><span class="sxs-lookup"><span data-stu-id="21d46-119">None</span></span>
<span data-ttu-id="21d46-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21d46-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21d46-121">출력</span><span class="sxs-lookup"><span data-stu-id="21d46-121">OUTPUTS</span></span>

### <span data-ttu-id="21d46-122">System.webserver. List ' 1 [SiteRecovery. e \ 자격 증명 모음]</span><span class="sxs-lookup"><span data-stu-id="21d46-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="21d46-123">상속자</span><span class="sxs-lookup"><span data-stu-id="21d46-123">NOTES</span></span>

## <span data-ttu-id="21d46-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21d46-124">RELATED LINKS</span></span>

[<span data-ttu-id="21d46-125">새로운 AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="21d46-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="21d46-126">제거-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="21d46-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
