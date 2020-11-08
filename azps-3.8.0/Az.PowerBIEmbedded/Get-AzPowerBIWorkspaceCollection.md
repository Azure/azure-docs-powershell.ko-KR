---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034127"
---
# <span data-ttu-id="b44f5-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b44f5-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="b44f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b44f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b44f5-103">Power BI 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="b44f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b44f5-104">SYNTAX</span></span>

### <span data-ttu-id="b44f5-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b44f5-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b44f5-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b44f5-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b44f5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b44f5-107">DESCRIPTION</span></span>
<span data-ttu-id="b44f5-108">**AzPowerBIWorkspaceCollection** Cmdlet은 Azure 구독, 리소스 그룹 또는 컬렉션 이름에서 Power BI 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="b44f5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b44f5-109">EXAMPLES</span></span>

### <span data-ttu-id="b44f5-110">예제 1: 리소스 그룹의 모든 작업 영역 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="b44f5-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="b44f5-111">이 명령은 ResourceGroup17 이라는 리소스 그룹에 속하는 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="b44f5-112">예제 2: 이름을 사용 하 여 작업 영역 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="b44f5-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b44f5-113">이 명령은 지정 된 리소스 그룹에서 WCN11 이라는 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b44f5-114">변수</span><span class="sxs-lookup"><span data-stu-id="b44f5-114">PARAMETERS</span></span>

### <span data-ttu-id="b44f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44f5-115">-DefaultProfile</span></span>
<span data-ttu-id="b44f5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b44f5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b44f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b44f5-118">이 cmdlet이 작업 영역 컬렉션을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44f5-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b44f5-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b44f5-120">이 cmdlet이 가져오는 Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44f5-121">CommonParameters</span></span>
<span data-ttu-id="b44f5-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b44f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44f5-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44f5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44f5-124">입력</span><span class="sxs-lookup"><span data-stu-id="b44f5-124">INPUTS</span></span>

### <span data-ttu-id="b44f5-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b44f5-125">System.String</span></span>

## <span data-ttu-id="b44f5-126">출력</span><span class="sxs-lookup"><span data-stu-id="b44f5-126">OUTPUTS</span></span>

### <span data-ttu-id="b44f5-127">PSWorkspaceCollection. PowerBIEmbedded. \*.</span><span class="sxs-lookup"><span data-stu-id="b44f5-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="b44f5-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b44f5-128">NOTES</span></span>

## <span data-ttu-id="b44f5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b44f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="b44f5-130">새로운 AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b44f5-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="b44f5-131">제거-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b44f5-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


