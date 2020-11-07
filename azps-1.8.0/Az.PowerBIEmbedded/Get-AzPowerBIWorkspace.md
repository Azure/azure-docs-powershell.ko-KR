---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 0bba0651d8b1125673b97aea625a11e598db6c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699818"
---
# <span data-ttu-id="0c1cc-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c1cc-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="0c1cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1cc-103">Power BI workspace 컬렉션의 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0c1cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c1cc-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c1cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c1cc-105">DESCRIPTION</span></span>
<span data-ttu-id="0c1cc-106">**AzPowerBIWorkspace** Cmdlet은 Power BI workspace 컬렉션의 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0c1cc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0c1cc-107">EXAMPLES</span></span>

### <span data-ttu-id="0c1cc-108">예제 1: 작업 영역 컬렉션의 작업 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="0c1cc-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0c1cc-109">이 명령은 지정 된 리소스 그룹의 WCN11 이라는 작업 영역 컬렉션에 속한 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0c1cc-110">변수</span><span class="sxs-lookup"><span data-stu-id="0c1cc-110">PARAMETERS</span></span>

### <span data-ttu-id="0c1cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1cc-111">-DefaultProfile</span></span>
<span data-ttu-id="0c1cc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c1cc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c1cc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c1cc-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c1cc-114">작업 영역 컬렉션이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="0c1cc-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0c1cc-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0c1cc-116">이 cmdlet이 작업 영역을 가져오는 작업 영역 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="0c1cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1cc-117">CommonParameters</span></span>
<span data-ttu-id="0c1cc-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1cc-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1cc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1cc-120">입력</span><span class="sxs-lookup"><span data-stu-id="0c1cc-120">INPUTS</span></span>

### <span data-ttu-id="0c1cc-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c1cc-121">System.String</span></span>

## <span data-ttu-id="0c1cc-122">출력</span><span class="sxs-lookup"><span data-stu-id="0c1cc-122">OUTPUTS</span></span>

### <span data-ttu-id="0c1cc-123">Microsoft. i. i. m a m.</span><span class="sxs-lookup"><span data-stu-id="0c1cc-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="0c1cc-124">상속자</span><span class="sxs-lookup"><span data-stu-id="0c1cc-124">NOTES</span></span>

## <span data-ttu-id="0c1cc-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c1cc-125">RELATED LINKS</span></span>

[<span data-ttu-id="0c1cc-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0c1cc-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


