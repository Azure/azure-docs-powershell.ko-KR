---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703616"
---
# <span data-ttu-id="c26d4-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c26d4-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="c26d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c26d4-103">현재 구독에서 사이트 복구 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c26d4-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c26d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c26d4-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c26d4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c26d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c26d4-106">**AzureRmSiteRecoveryVault** cmdlet은 현재 구독에서 Azure site recovery 자격 증명 모음 또는 특정 사이트 복구 자격 증명 모음 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c26d4-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="c26d4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c26d4-107">EXAMPLES</span></span>

## <span data-ttu-id="c26d4-108">변수</span><span class="sxs-lookup"><span data-stu-id="c26d4-108">PARAMETERS</span></span>

### <span data-ttu-id="c26d4-109">-이름</span><span class="sxs-lookup"><span data-stu-id="c26d4-109">-Name</span></span>
<span data-ttu-id="c26d4-110">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26d4-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26d4-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26d4-111">-ResourceGroupName</span></span>
<span data-ttu-id="c26d4-112">복구 서비스 개체를 가져올 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26d4-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26d4-113">-DefaultProfile</span></span>
<span data-ttu-id="c26d4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c26d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26d4-115">CommonParameters</span></span>
<span data-ttu-id="c26d4-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c26d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26d4-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26d4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26d4-118">입력</span><span class="sxs-lookup"><span data-stu-id="c26d4-118">INPUTS</span></span>

## <span data-ttu-id="c26d4-119">출력</span><span class="sxs-lookup"><span data-stu-id="c26d4-119">OUTPUTS</span></span>

### <span data-ttu-id="c26d4-120">System.webserver. List ' 1 [SiteRecovery. e \ 자격 증명 모음]</span><span class="sxs-lookup"><span data-stu-id="c26d4-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="c26d4-121">상속자</span><span class="sxs-lookup"><span data-stu-id="c26d4-121">NOTES</span></span>

## <span data-ttu-id="c26d4-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c26d4-122">RELATED LINKS</span></span>

[<span data-ttu-id="c26d4-123">새로운 AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c26d4-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="c26d4-124">제거-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c26d4-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
