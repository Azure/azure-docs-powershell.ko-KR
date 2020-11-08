---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056373"
---
# <span data-ttu-id="95949-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="95949-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="95949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95949-102">SYNOPSIS</span></span>
<span data-ttu-id="95949-103">Azure DevSpaces 컨트롤러를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="95949-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="95949-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95949-104">SYNTAX</span></span>

### <span data-ttu-id="95949-105">ListDevSpacesControllerParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="95949-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95949-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95949-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95949-107">설명은</span><span class="sxs-lookup"><span data-stu-id="95949-107">DESCRIPTION</span></span>
<span data-ttu-id="95949-108">Azure DevSpaces 컨트롤러를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="95949-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="95949-109">예제의</span><span class="sxs-lookup"><span data-stu-id="95949-109">EXAMPLES</span></span>

### <span data-ttu-id="95949-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="95949-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="95949-111">구독의 모든 컨트롤러를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="95949-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="95949-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="95949-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="95949-113">구독에서 DevSpaces 컨트롤러를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95949-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="95949-114">변수</span><span class="sxs-lookup"><span data-stu-id="95949-114">PARAMETERS</span></span>

### <span data-ttu-id="95949-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95949-115">-DefaultProfile</span></span>
<span data-ttu-id="95949-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95949-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95949-117">-이름</span><span class="sxs-lookup"><span data-stu-id="95949-117">-Name</span></span>
<span data-ttu-id="95949-118">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95949-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95949-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95949-119">-ResourceGroupName</span></span>
<span data-ttu-id="95949-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="95949-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95949-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95949-121">CommonParameters</span></span>
<span data-ttu-id="95949-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95949-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95949-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95949-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95949-124">입력</span><span class="sxs-lookup"><span data-stu-id="95949-124">INPUTS</span></span>

### <span data-ttu-id="95949-125">않아야</span><span class="sxs-lookup"><span data-stu-id="95949-125">None</span></span>

## <span data-ttu-id="95949-126">출력</span><span class="sxs-lookup"><span data-stu-id="95949-126">OUTPUTS</span></span>

### <span data-ttu-id="95949-127">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="95949-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="95949-128">상속자</span><span class="sxs-lookup"><span data-stu-id="95949-128">NOTES</span></span>

## <span data-ttu-id="95949-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95949-129">RELATED LINKS</span></span>
