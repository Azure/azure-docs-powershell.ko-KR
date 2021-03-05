---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 6937d79d6f60c053238075713f5d58432124e7e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988171"
---
# <span data-ttu-id="593df-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="593df-101">Get-AzIotHub</span></span>

## <span data-ttu-id="593df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="593df-102">SYNOPSIS</span></span>
<span data-ttu-id="593df-103">구독에서 IotHubs에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="593df-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="593df-104">구문</span><span class="sxs-lookup"><span data-stu-id="593df-104">SYNTAX</span></span>

### <span data-ttu-id="593df-105">ListIotHubsByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="593df-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="593df-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="593df-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="593df-107">설명</span><span class="sxs-lookup"><span data-stu-id="593df-107">DESCRIPTION</span></span>
<span data-ttu-id="593df-108">구독에서 IotHubs에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="593df-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="593df-109">구독에서 모든 IotHub 인스턴스를 보거나 리소스 그룹 또는 특정 IotHub 이름으로 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="593df-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="593df-110">예제</span><span class="sxs-lookup"><span data-stu-id="593df-110">EXAMPLES</span></span>

### <span data-ttu-id="593df-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="593df-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="593df-112">구독에서 모든 IotHubs를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="593df-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="593df-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="593df-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="593df-114">"myresourcegroup"이라는 리소스 그룹에 속하는 구독의 모든 IotHubs를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="593df-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="593df-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="593df-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="593df-116">"myiothub"라는 IotHub에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="593df-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="593df-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="593df-117">PARAMETERS</span></span>

### <span data-ttu-id="593df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593df-118">-DefaultProfile</span></span>
<span data-ttu-id="593df-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="593df-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="593df-120">-Name</span><span class="sxs-lookup"><span data-stu-id="593df-120">-Name</span></span>
<span data-ttu-id="593df-121">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="593df-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="593df-122">-ResourceGroupName</span></span>
<span data-ttu-id="593df-123">ResourceGroup의 이름</span><span class="sxs-lookup"><span data-stu-id="593df-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593df-124">CommonParameters</span></span>
<span data-ttu-id="593df-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="593df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593df-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="593df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593df-127">입력</span><span class="sxs-lookup"><span data-stu-id="593df-127">INPUTS</span></span>

### <span data-ttu-id="593df-128">System.String</span><span class="sxs-lookup"><span data-stu-id="593df-128">System.String</span></span>

## <span data-ttu-id="593df-129">출력</span><span class="sxs-lookup"><span data-stu-id="593df-129">OUTPUTS</span></span>

### <span data-ttu-id="593df-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="593df-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="593df-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="593df-131">NOTES</span></span>

## <span data-ttu-id="593df-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="593df-132">RELATED LINKS</span></span>
