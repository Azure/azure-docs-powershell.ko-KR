---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355778"
---
# <span data-ttu-id="f709f-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f709f-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="f709f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f709f-102">SYNOPSIS</span></span>
<span data-ttu-id="f709f-103">Power BI 작업 영역 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="f709f-104">구문</span><span class="sxs-lookup"><span data-stu-id="f709f-104">SYNTAX</span></span>

### <span data-ttu-id="f709f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f709f-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f709f-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f709f-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f709f-107">설명</span><span class="sxs-lookup"><span data-stu-id="f709f-107">DESCRIPTION</span></span>
<span data-ttu-id="f709f-108">**Get-AzPowerBIWorkspaceCollection** cmdlet은 Azure 구독 및 리소스 그룹 또는 컬렉션 이름으로 Power BI 작업 영역 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="f709f-109">예제</span><span class="sxs-lookup"><span data-stu-id="f709f-109">EXAMPLES</span></span>

### <span data-ttu-id="f709f-110">예제 1: 리소스 그룹의 모든 작업 영역 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="f709f-111">이 명령은 ResourceGroup17이라는 리소스 그룹에 속하는 작업 영역 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="f709f-112">예제 2: 이름을 사용하여 작업 영역 컬렉션을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="f709f-113">이 명령은 지정된 리소스 그룹에서 WCN11이라는 작업 영역 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="f709f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f709f-114">PARAMETERS</span></span>

### <span data-ttu-id="f709f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f709f-115">-DefaultProfile</span></span>
<span data-ttu-id="f709f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f709f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f709f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f709f-117">-ResourceGroupName</span></span>
<span data-ttu-id="f709f-118">이 cmdlet에서 작업 영역 컬렉션을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="f709f-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="f709f-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="f709f-120">이 cmdlet에서 얻을 수 있는 Power BI 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f709f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f709f-121">CommonParameters</span></span>
<span data-ttu-id="f709f-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f709f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f709f-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f709f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f709f-124">입력</span><span class="sxs-lookup"><span data-stu-id="f709f-124">INPUTS</span></span>

### <span data-ttu-id="f709f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f709f-125">System.String</span></span>

## <span data-ttu-id="f709f-126">출력</span><span class="sxs-lookup"><span data-stu-id="f709f-126">OUTPUTS</span></span>

### <span data-ttu-id="f709f-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f709f-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="f709f-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f709f-128">NOTES</span></span>

## <span data-ttu-id="f709f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f709f-129">RELATED LINKS</span></span>

[<span data-ttu-id="f709f-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f709f-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="f709f-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f709f-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


