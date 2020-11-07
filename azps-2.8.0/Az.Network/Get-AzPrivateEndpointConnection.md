---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870110"
---
# <span data-ttu-id="bd7cd-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bd7cd-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="bd7cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7cd-103">개인 끝점 연결 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="bd7cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd7cd-104">SYNTAX</span></span>

### <span data-ttu-id="bd7cd-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="bd7cd-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd7cd-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="bd7cd-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7cd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bd7cd-107">DESCRIPTION</span></span>
<span data-ttu-id="bd7cd-108">**Get-AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="bd7cd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bd7cd-109">EXAMPLES</span></span>

### <span data-ttu-id="bd7cd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd7cd-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="bd7cd-111">이 예제에서는 MyPrivateEndpointConnection1 라는 개인 끝점 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="bd7cd-112">변수</span><span class="sxs-lookup"><span data-stu-id="bd7cd-112">PARAMETERS</span></span>

### <span data-ttu-id="bd7cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7cd-113">-DefaultProfile</span></span>
<span data-ttu-id="bd7cd-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd7cd-115">-설명</span><span class="sxs-lookup"><span data-stu-id="bd7cd-115">-Description</span></span>
<span data-ttu-id="bd7cd-116">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7cd-117">-이름</span><span class="sxs-lookup"><span data-stu-id="bd7cd-117">-Name</span></span>
<span data-ttu-id="bd7cd-118">개인 끝점 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-118">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd7cd-120">개인 끝점 연결의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="bd7cd-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7cd-121">-ResourceId</span></span>
<span data-ttu-id="bd7cd-122">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-122">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7cd-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bd7cd-123">-ServiceName</span></span>
<span data-ttu-id="bd7cd-124">개인 끝점 연결이 있는 개인 링크 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="bd7cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7cd-125">CommonParameters</span></span>
<span data-ttu-id="bd7cd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7cd-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd7cd-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7cd-128">입력</span><span class="sxs-lookup"><span data-stu-id="bd7cd-128">INPUTS</span></span>

### <span data-ttu-id="bd7cd-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bd7cd-129">System.String</span></span>

## <span data-ttu-id="bd7cd-130">출력</span><span class="sxs-lookup"><span data-stu-id="bd7cd-130">OUTPUTS</span></span>

### <span data-ttu-id="bd7cd-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bd7cd-131">System.Boolean</span></span>

## <span data-ttu-id="bd7cd-132">상속자</span><span class="sxs-lookup"><span data-stu-id="bd7cd-132">NOTES</span></span>

## <span data-ttu-id="bd7cd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd7cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="bd7cd-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bd7cd-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
