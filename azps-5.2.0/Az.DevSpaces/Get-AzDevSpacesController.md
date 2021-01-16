---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328922"
---
# <span data-ttu-id="5d59d-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="5d59d-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="5d59d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d59d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d59d-103">Azure DevSpaces 컨트롤러를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="5d59d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d59d-104">SYNTAX</span></span>

### <span data-ttu-id="5d59d-105">ListDevSpacesControllerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d59d-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d59d-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d59d-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d59d-107">설명</span><span class="sxs-lookup"><span data-stu-id="5d59d-107">DESCRIPTION</span></span>
<span data-ttu-id="5d59d-108">Azure DevSpaces 컨트롤러를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="5d59d-109">예제</span><span class="sxs-lookup"><span data-stu-id="5d59d-109">EXAMPLES</span></span>

### <span data-ttu-id="5d59d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d59d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="5d59d-111">구독의 모든 컨트롤러를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="5d59d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5d59d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="5d59d-113">구독에서 DevSpaces 컨트롤러를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="5d59d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d59d-114">PARAMETERS</span></span>

### <span data-ttu-id="5d59d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d59d-115">-DefaultProfile</span></span>
<span data-ttu-id="5d59d-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d59d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5d59d-117">-Name</span></span>
<span data-ttu-id="5d59d-118">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="5d59d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d59d-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d59d-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5d59d-120">Resource group name</span></span>

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

### <span data-ttu-id="5d59d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d59d-121">CommonParameters</span></span>
<span data-ttu-id="5d59d-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d59d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d59d-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d59d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d59d-124">입력</span><span class="sxs-lookup"><span data-stu-id="5d59d-124">INPUTS</span></span>

### <span data-ttu-id="5d59d-125">없음</span><span class="sxs-lookup"><span data-stu-id="5d59d-125">None</span></span>

## <span data-ttu-id="5d59d-126">출력</span><span class="sxs-lookup"><span data-stu-id="5d59d-126">OUTPUTS</span></span>

### <span data-ttu-id="5d59d-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="5d59d-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="5d59d-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d59d-128">NOTES</span></span>

## <span data-ttu-id="5d59d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d59d-129">RELATED LINKS</span></span>
