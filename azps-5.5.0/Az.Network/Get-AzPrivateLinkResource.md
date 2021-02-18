---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184721"
---
# <span data-ttu-id="7c22f-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7c22f-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="7c22f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c22f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c22f-103">개인 링크 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-103">Gets a private link resource.</span></span>

## <span data-ttu-id="7c22f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c22f-104">SYNTAX</span></span>

### <span data-ttu-id="7c22f-105">ByPrivateLinkResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c22f-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c22f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7c22f-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c22f-107">설명</span><span class="sxs-lookup"><span data-stu-id="7c22f-107">DESCRIPTION</span></span>
<span data-ttu-id="7c22f-108">**Get-AzPrivateLinkResource** cmdlet은 PrivateLinkResource에 속하는 모든 링크 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="7c22f-109">예제</span><span class="sxs-lookup"><span data-stu-id="7c22f-109">EXAMPLES</span></span>

### <span data-ttu-id="7c22f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c22f-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="7c22f-111">이 예제에서는 mySql이라는 sql Server에 대한 모든 개인 링크 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="7c22f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c22f-112">PARAMETERS</span></span>

### <span data-ttu-id="7c22f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c22f-113">-DefaultProfile</span></span>
<span data-ttu-id="7c22f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c22f-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7c22f-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="7c22f-116">개인 링크 리소스의 Azure 리소스 관리자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="7c22f-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7c22f-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7c22f-118">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-118">The private link resource type.</span></span>

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

### <span data-ttu-id="7c22f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c22f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c22f-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-120">The resource group name.</span></span>

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

### <span data-ttu-id="7c22f-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c22f-121">-ServiceName</span></span>
<span data-ttu-id="7c22f-122">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-122">The private link service name.</span></span>

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

### <span data-ttu-id="7c22f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c22f-123">CommonParameters</span></span>
<span data-ttu-id="7c22f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c22f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c22f-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c22f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c22f-126">입력</span><span class="sxs-lookup"><span data-stu-id="7c22f-126">INPUTS</span></span>

### <span data-ttu-id="7c22f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7c22f-127">System.String</span></span>

## <span data-ttu-id="7c22f-128">출력</span><span class="sxs-lookup"><span data-stu-id="7c22f-128">OUTPUTS</span></span>

### <span data-ttu-id="7c22f-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c22f-129">System.Boolean</span></span>

## <span data-ttu-id="7c22f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c22f-130">NOTES</span></span>

## <span data-ttu-id="7c22f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c22f-131">RELATED LINKS</span></span>
