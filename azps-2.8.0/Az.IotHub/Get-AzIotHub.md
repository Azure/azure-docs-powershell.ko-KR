---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689749"
---
# <span data-ttu-id="716eb-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="716eb-101">Get-AzIotHub</span></span>

## <span data-ttu-id="716eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="716eb-102">SYNOPSIS</span></span>
<span data-ttu-id="716eb-103">구독에서 IotHubs에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="716eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="716eb-104">SYNTAX</span></span>

### <span data-ttu-id="716eb-105">ListIotHubsByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="716eb-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="716eb-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="716eb-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="716eb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="716eb-107">DESCRIPTION</span></span>
<span data-ttu-id="716eb-108">구독에서 IotHubs에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="716eb-109">구독에서 모든 IotHub 인스턴스를 보거나 리소스 그룹 또는 특정 IotHub 이름을 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="716eb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="716eb-110">EXAMPLES</span></span>

### <span data-ttu-id="716eb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="716eb-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="716eb-112">구독에 있는 모든 IotHubs를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="716eb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="716eb-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="716eb-114">"Myresourcegroup" 이라는 리소스 이름에 속하는 구독의 모든 IotHubs를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="716eb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="716eb-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="716eb-116">이름이 "myiothub" 인 IotHub에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="716eb-117">변수</span><span class="sxs-lookup"><span data-stu-id="716eb-117">PARAMETERS</span></span>

### <span data-ttu-id="716eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716eb-118">-DefaultProfile</span></span>
<span data-ttu-id="716eb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="716eb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="716eb-120">-이름</span><span class="sxs-lookup"><span data-stu-id="716eb-120">-Name</span></span>
<span data-ttu-id="716eb-121">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="716eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="716eb-123">ResourceGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="716eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716eb-124">CommonParameters</span></span>
<span data-ttu-id="716eb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="716eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716eb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716eb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716eb-127">입력</span><span class="sxs-lookup"><span data-stu-id="716eb-127">INPUTS</span></span>

### <span data-ttu-id="716eb-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="716eb-128">System.String</span></span>

## <span data-ttu-id="716eb-129">출력</span><span class="sxs-lookup"><span data-stu-id="716eb-129">OUTPUTS</span></span>

### <span data-ttu-id="716eb-130">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="716eb-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="716eb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="716eb-131">NOTES</span></span>

## <span data-ttu-id="716eb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="716eb-132">RELATED LINKS</span></span>
