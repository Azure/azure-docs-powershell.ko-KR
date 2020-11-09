---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309610"
---
# <span data-ttu-id="a9000-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a9000-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="a9000-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9000-102">SYNOPSIS</span></span>
<span data-ttu-id="a9000-103">개인 링크 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-103">Gets a private link resource.</span></span>

## <span data-ttu-id="a9000-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9000-104">SYNTAX</span></span>

### <span data-ttu-id="a9000-105">ByPrivateLinkResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9000-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9000-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a9000-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9000-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a9000-107">DESCRIPTION</span></span>
<span data-ttu-id="a9000-108">AzPrivateLinkResource cmdlet은 모든 링크 리소스 (PrivateLinkResource **)** 를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="a9000-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a9000-109">EXAMPLES</span></span>

### <span data-ttu-id="a9000-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9000-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a9000-111">이 예제에서는 nbelong 이름이 mySql 인 sql server에 속하는 모든 비공개 링크 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="a9000-112">변수</span><span class="sxs-lookup"><span data-stu-id="a9000-112">PARAMETERS</span></span>

### <span data-ttu-id="a9000-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9000-113">-DefaultProfile</span></span>
<span data-ttu-id="a9000-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9000-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a9000-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a9000-116">개인 링크 리소스의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="a9000-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a9000-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a9000-118">개인 링크 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-118">The private link resource type.</span></span>

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

### <span data-ttu-id="a9000-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9000-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9000-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-120">The resource group name.</span></span>

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

### <span data-ttu-id="a9000-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a9000-121">-ServiceName</span></span>
<span data-ttu-id="a9000-122">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-122">The private link service name.</span></span>

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

### <span data-ttu-id="a9000-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9000-123">CommonParameters</span></span>
<span data-ttu-id="a9000-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9000-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9000-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9000-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9000-126">입력</span><span class="sxs-lookup"><span data-stu-id="a9000-126">INPUTS</span></span>

### <span data-ttu-id="a9000-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9000-127">System.String</span></span>

## <span data-ttu-id="a9000-128">출력</span><span class="sxs-lookup"><span data-stu-id="a9000-128">OUTPUTS</span></span>

### <span data-ttu-id="a9000-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a9000-129">System.Boolean</span></span>

## <span data-ttu-id="a9000-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a9000-130">NOTES</span></span>

## <span data-ttu-id="a9000-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9000-131">RELATED LINKS</span></span>
