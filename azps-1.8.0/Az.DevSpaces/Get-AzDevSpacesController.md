---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 7cc4c61073b0b196faca8d95bd5153abe2587ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700965"
---
# <span data-ttu-id="7f062-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="7f062-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="7f062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f062-102">SYNOPSIS</span></span>
<span data-ttu-id="7f062-103">Azure DevSpaces 컨트롤러를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="7f062-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f062-104">SYNTAX</span></span>

### <span data-ttu-id="7f062-105">ListDevSpacesControllerParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f062-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f062-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f062-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f062-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7f062-107">DESCRIPTION</span></span>
<span data-ttu-id="7f062-108">Azure DevSpaces 컨트롤러를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="7f062-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7f062-109">EXAMPLES</span></span>

### <span data-ttu-id="7f062-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f062-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="7f062-111">구독의 모든 컨트롤러를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="7f062-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7f062-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="7f062-113">구독에서 DevSpaces 컨트롤러를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="7f062-114">변수</span><span class="sxs-lookup"><span data-stu-id="7f062-114">PARAMETERS</span></span>

### <span data-ttu-id="7f062-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f062-115">-DefaultProfile</span></span>
<span data-ttu-id="7f062-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f062-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7f062-117">-Name</span></span>
<span data-ttu-id="7f062-118">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="7f062-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f062-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f062-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7f062-120">Resource group name</span></span>

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

### <span data-ttu-id="7f062-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f062-121">CommonParameters</span></span>
<span data-ttu-id="7f062-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f062-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f062-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f062-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f062-124">입력</span><span class="sxs-lookup"><span data-stu-id="7f062-124">INPUTS</span></span>

### <span data-ttu-id="7f062-125">않아야</span><span class="sxs-lookup"><span data-stu-id="7f062-125">None</span></span>

## <span data-ttu-id="7f062-126">출력</span><span class="sxs-lookup"><span data-stu-id="7f062-126">OUTPUTS</span></span>

### <span data-ttu-id="7f062-127">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="7f062-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="7f062-128">상속자</span><span class="sxs-lookup"><span data-stu-id="7f062-128">NOTES</span></span>

## <span data-ttu-id="7f062-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f062-129">RELATED LINKS</span></span>
