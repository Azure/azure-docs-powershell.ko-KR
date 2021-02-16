---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179073"
---
# <span data-ttu-id="1d445-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d445-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="1d445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d445-102">SYNOPSIS</span></span>
<span data-ttu-id="1d445-103">Power BI 작업 영역 컬렉션에서 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d445-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="1d445-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d445-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d445-105">설명</span><span class="sxs-lookup"><span data-stu-id="1d445-105">DESCRIPTION</span></span>
<span data-ttu-id="1d445-106">**Get-AzPowerBIWorkspace** cmdlet은 Power BI 작업 영역 컬렉션에 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d445-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="1d445-107">예제</span><span class="sxs-lookup"><span data-stu-id="1d445-107">EXAMPLES</span></span>

### <span data-ttu-id="1d445-108">예제 1: 작업 영역 컬렉션의 작업 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="1d445-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1d445-109">이 명령은 지정된 리소스 그룹에 있는 WCN11이라는 작업 영역 컬렉션에 속하는 작업 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="1d445-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1d445-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d445-110">PARAMETERS</span></span>

### <span data-ttu-id="1d445-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d445-111">-DefaultProfile</span></span>
<span data-ttu-id="1d445-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1d445-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d445-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d445-113">-ResourceGroupName</span></span>
<span data-ttu-id="1d445-114">작업 영역 컬렉션이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d445-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="1d445-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1d445-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1d445-116">이 cmdlet에서 작업 영역이 있는 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d445-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="1d445-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d445-117">CommonParameters</span></span>
<span data-ttu-id="1d445-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d445-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d445-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d445-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d445-120">입력</span><span class="sxs-lookup"><span data-stu-id="1d445-120">INPUTS</span></span>

### <span data-ttu-id="1d445-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1d445-121">System.String</span></span>

## <span data-ttu-id="1d445-122">출력</span><span class="sxs-lookup"><span data-stu-id="1d445-122">OUTPUTS</span></span>

### <span data-ttu-id="1d445-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d445-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="1d445-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d445-124">NOTES</span></span>

## <span data-ttu-id="1d445-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d445-125">RELATED LINKS</span></span>

[<span data-ttu-id="1d445-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1d445-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


