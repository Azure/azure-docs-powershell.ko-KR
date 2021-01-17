---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346742"
---
# <span data-ttu-id="b1d35-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="b1d35-101">Get-AzIotHub</span></span>

## <span data-ttu-id="b1d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1d35-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d35-103">구독의 IotHubs에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="b1d35-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1d35-104">SYNTAX</span></span>

### <span data-ttu-id="b1d35-105">ListIotHubsByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1d35-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1d35-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="b1d35-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1d35-107">설명</span><span class="sxs-lookup"><span data-stu-id="b1d35-107">DESCRIPTION</span></span>
<span data-ttu-id="b1d35-108">구독의 IotHubs에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="b1d35-109">구독의 모든 IotHub 인스턴스를 보거나 리소스 그룹 또는 특정 IotHub 이름으로 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="b1d35-110">예제</span><span class="sxs-lookup"><span data-stu-id="b1d35-110">EXAMPLES</span></span>

### <span data-ttu-id="b1d35-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1d35-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="b1d35-112">구독의 모든 IotHubs를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="b1d35-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b1d35-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="b1d35-114">"myresourcegroup"이라는 리소스 그룹에 속한 구독의 모든 IotHubs를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="b1d35-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="b1d35-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b1d35-116">"myiothub"라는 IotHub에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="b1d35-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1d35-117">PARAMETERS</span></span>

### <span data-ttu-id="b1d35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d35-118">-DefaultProfile</span></span>
<span data-ttu-id="b1d35-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b1d35-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1d35-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b1d35-120">-Name</span></span>
<span data-ttu-id="b1d35-121">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="b1d35-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b1d35-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d35-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1d35-123">ResourceGroup의 이름</span><span class="sxs-lookup"><span data-stu-id="b1d35-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="b1d35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d35-124">CommonParameters</span></span>
<span data-ttu-id="b1d35-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d35-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b1d35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d35-127">입력</span><span class="sxs-lookup"><span data-stu-id="b1d35-127">INPUTS</span></span>

### <span data-ttu-id="b1d35-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1d35-128">System.String</span></span>

## <span data-ttu-id="b1d35-129">출력</span><span class="sxs-lookup"><span data-stu-id="b1d35-129">OUTPUTS</span></span>

### <span data-ttu-id="b1d35-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b1d35-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="b1d35-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1d35-131">NOTES</span></span>

## <span data-ttu-id="b1d35-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1d35-132">RELATED LINKS</span></span>
