---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204015"
---
# <span data-ttu-id="bb202-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="bb202-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="bb202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb202-102">SYNOPSIS</span></span>
<span data-ttu-id="bb202-103">개인 링크 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb202-103">Gets a private link resource.</span></span>

## <span data-ttu-id="bb202-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb202-104">SYNTAX</span></span>

### <span data-ttu-id="bb202-105">ByPrivateLinkResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb202-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb202-106">설명은</span><span class="sxs-lookup"><span data-stu-id="bb202-106">DESCRIPTION</span></span>
<span data-ttu-id="bb202-107">AzPrivateLinkResource cmdlet은 모든 링크 리소스 (PrivateLinkResource **)** 를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb202-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="bb202-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bb202-108">EXAMPLES</span></span>

### <span data-ttu-id="bb202-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb202-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="bb202-110">이 예제에서는 nbelong 이름이 mySql 인 sql server에 속하는 모든 비공개 링크 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb202-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="bb202-111">변수</span><span class="sxs-lookup"><span data-stu-id="bb202-111">PARAMETERS</span></span>

### <span data-ttu-id="bb202-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb202-112">-DefaultProfile</span></span>
<span data-ttu-id="bb202-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb202-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb202-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bb202-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bb202-115">개인 링크 리소스의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="bb202-115">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb202-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb202-116">CommonParameters</span></span>
<span data-ttu-id="bb202-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb202-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb202-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb202-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb202-119">입력</span><span class="sxs-lookup"><span data-stu-id="bb202-119">INPUTS</span></span>

### <span data-ttu-id="bb202-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb202-120">System.String</span></span>

## <span data-ttu-id="bb202-121">출력</span><span class="sxs-lookup"><span data-stu-id="bb202-121">OUTPUTS</span></span>

### <span data-ttu-id="bb202-122">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bb202-122">System.Boolean</span></span>

## <span data-ttu-id="bb202-123">상속자</span><span class="sxs-lookup"><span data-stu-id="bb202-123">NOTES</span></span>

## <span data-ttu-id="bb202-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb202-124">RELATED LINKS</span></span>
