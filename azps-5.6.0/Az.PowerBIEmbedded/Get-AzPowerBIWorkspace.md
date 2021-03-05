---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: d9c93bc487817d99b217519453dea10543852a1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974619"
---
# <span data-ttu-id="6d0d2-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d0d2-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="6d0d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0d2-103">Power BI 작업 영역 컬렉션에서 작업 영역이 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="6d0d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d0d2-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d0d2-105">설명</span><span class="sxs-lookup"><span data-stu-id="6d0d2-105">DESCRIPTION</span></span>
<span data-ttu-id="6d0d2-106">**Get-AzPowerBIWorkspace** cmdlet은 Power BI 작업 영역 컬렉션에서 작업 영역이 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="6d0d2-107">예제</span><span class="sxs-lookup"><span data-stu-id="6d0d2-107">EXAMPLES</span></span>

### <span data-ttu-id="6d0d2-108">예제 1: 작업 영역 컬렉션의 작업 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="6d0d2-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="6d0d2-109">이 명령은 지정된 리소스 그룹의 WCN11이라는 작업 영역 컬렉션에 속하는 작업 영역이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="6d0d2-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d0d2-110">PARAMETERS</span></span>

### <span data-ttu-id="6d0d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0d2-111">-DefaultProfile</span></span>
<span data-ttu-id="6d0d2-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6d0d2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d0d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d0d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="6d0d2-114">작업 영역 컬렉션이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0d2-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="6d0d2-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="6d0d2-116">이 cmdlet에서 작업 영역이 있는 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0d2-117">CommonParameters</span></span>
<span data-ttu-id="6d0d2-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0d2-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d0d2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0d2-120">입력</span><span class="sxs-lookup"><span data-stu-id="6d0d2-120">INPUTS</span></span>

### <span data-ttu-id="6d0d2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6d0d2-121">System.String</span></span>

## <span data-ttu-id="6d0d2-122">출력</span><span class="sxs-lookup"><span data-stu-id="6d0d2-122">OUTPUTS</span></span>

### <span data-ttu-id="6d0d2-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d0d2-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="6d0d2-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d0d2-124">NOTES</span></span>

## <span data-ttu-id="6d0d2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d0d2-125">RELATED LINKS</span></span>

[<span data-ttu-id="6d0d2-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6d0d2-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


