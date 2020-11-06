---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c7beab54a416809a3f5edd033d4c7946a16b807b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536267"
---
# <span data-ttu-id="5d40f-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d40f-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="5d40f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d40f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d40f-103">Power BI workspace 컬렉션의 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d40f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d40f-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d40f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d40f-105">DESCRIPTION</span></span>
<span data-ttu-id="5d40f-106">**AzureRmPowerBIWorkspace** Cmdlet은 Power BI workspace 컬렉션의 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="5d40f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5d40f-107">EXAMPLES</span></span>

### <span data-ttu-id="5d40f-108">예제 1: 작업 영역 컬렉션의 작업 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d40f-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="5d40f-109">이 명령은 지정 된 리소스 그룹의 WCN11 이라는 작업 영역 컬렉션에 속한 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="5d40f-110">변수</span><span class="sxs-lookup"><span data-stu-id="5d40f-110">PARAMETERS</span></span>

### <span data-ttu-id="5d40f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d40f-111">-ResourceGroupName</span></span>
<span data-ttu-id="5d40f-112">작업 영역 컬렉션이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-112">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="5d40f-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="5d40f-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="5d40f-114">이 cmdlet이 작업 영역을 가져오는 작업 영역 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-114">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="5d40f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d40f-115">-DefaultProfile</span></span>
<span data-ttu-id="5d40f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d40f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d40f-117">CommonParameters</span></span>
<span data-ttu-id="5d40f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d40f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d40f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d40f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d40f-120">입력</span><span class="sxs-lookup"><span data-stu-id="5d40f-120">INPUTS</span></span>

## <span data-ttu-id="5d40f-121">출력</span><span class="sxs-lookup"><span data-stu-id="5d40f-121">OUTPUTS</span></span>

### <span data-ttu-id="5d40f-122">Microsoft. i. i. m a m.</span><span class="sxs-lookup"><span data-stu-id="5d40f-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="5d40f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="5d40f-123">NOTES</span></span>

## <span data-ttu-id="5d40f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d40f-124">RELATED LINKS</span></span>

[<span data-ttu-id="5d40f-125">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="5d40f-125">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


