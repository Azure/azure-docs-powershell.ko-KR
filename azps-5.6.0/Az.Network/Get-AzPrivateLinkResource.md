---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 5c341677f5bc741f5848508f80b1a29e29c90b17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954203"
---
# <span data-ttu-id="c99b1-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="c99b1-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="c99b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c99b1-103">개인 링크 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-103">Gets a private link resource.</span></span>

## <span data-ttu-id="c99b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="c99b1-104">SYNTAX</span></span>

### <span data-ttu-id="c99b1-105">ByPrivateLinkResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="c99b1-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c99b1-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="c99b1-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="c99b1-107">설명</span><span class="sxs-lookup"><span data-stu-id="c99b1-107">DESCRIPTION</span></span>
<span data-ttu-id="c99b1-108">**Get-AzPrivateLinkResource** cmdlet은 PrivateLinkResource에 속하는 모든 링크 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="c99b1-109">예제</span><span class="sxs-lookup"><span data-stu-id="c99b1-109">EXAMPLES</span></span>

### <span data-ttu-id="c99b1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c99b1-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="c99b1-111">이 예제에서는 mySql이라는 sql Server에 대한 모든 개인 링크 리소스 nbelong을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="c99b1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c99b1-112">PARAMETERS</span></span>

### <span data-ttu-id="c99b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99b1-113">-DefaultProfile</span></span>
<span data-ttu-id="c99b1-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c99b1-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="c99b1-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="c99b1-116">개인 링크 리소스의 Azure 리소스 관리자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="c99b1-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="c99b1-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="c99b1-118">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="c99b1-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b1-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c99b1-121">-ServiceName</span></span>
<span data-ttu-id="c99b1-122">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99b1-123">CommonParameters</span></span>
<span data-ttu-id="c99b1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c99b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99b1-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c99b1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99b1-126">입력</span><span class="sxs-lookup"><span data-stu-id="c99b1-126">INPUTS</span></span>

### <span data-ttu-id="c99b1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c99b1-127">System.String</span></span>

## <span data-ttu-id="c99b1-128">출력</span><span class="sxs-lookup"><span data-stu-id="c99b1-128">OUTPUTS</span></span>

### <span data-ttu-id="c99b1-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c99b1-129">System.Boolean</span></span>

## <span data-ttu-id="c99b1-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c99b1-130">NOTES</span></span>

## <span data-ttu-id="c99b1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c99b1-131">RELATED LINKS</span></span>
