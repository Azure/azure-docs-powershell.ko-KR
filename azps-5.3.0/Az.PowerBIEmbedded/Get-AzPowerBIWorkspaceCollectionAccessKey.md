---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492466"
---
# <span data-ttu-id="36b13-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="36b13-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="36b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b13-102">SYNOPSIS</span></span>
<span data-ttu-id="36b13-103">Power BI 작업 영역 컬렉션과 연결된 현재 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36b13-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="36b13-104">구문</span><span class="sxs-lookup"><span data-stu-id="36b13-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36b13-105">설명</span><span class="sxs-lookup"><span data-stu-id="36b13-105">DESCRIPTION</span></span>
<span data-ttu-id="36b13-106">**Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet은 Power BI 작업 영역 컬렉션과 연결된 현재 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36b13-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="36b13-107">예제</span><span class="sxs-lookup"><span data-stu-id="36b13-107">EXAMPLES</span></span>

### <span data-ttu-id="36b13-108">예제 1: 액세스 키 얻기</span><span class="sxs-lookup"><span data-stu-id="36b13-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="36b13-109">이 명령은 지정된 리소스 그룹의 WCN11이라는 작업 영역 컬렉션에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36b13-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="36b13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b13-110">PARAMETERS</span></span>

### <span data-ttu-id="36b13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b13-111">-DefaultProfile</span></span>
<span data-ttu-id="36b13-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="36b13-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36b13-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b13-113">-ResourceGroupName</span></span>
<span data-ttu-id="36b13-114">컬렉션의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b13-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="36b13-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="36b13-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="36b13-116">이 cmdlet이 작동하는 Power BI 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36b13-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="36b13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b13-117">CommonParameters</span></span>
<span data-ttu-id="36b13-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36b13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b13-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36b13-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b13-120">입력</span><span class="sxs-lookup"><span data-stu-id="36b13-120">INPUTS</span></span>

### <span data-ttu-id="36b13-121">System.String</span><span class="sxs-lookup"><span data-stu-id="36b13-121">System.String</span></span>

## <span data-ttu-id="36b13-122">출력</span><span class="sxs-lookup"><span data-stu-id="36b13-122">OUTPUTS</span></span>

### <span data-ttu-id="36b13-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="36b13-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="36b13-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36b13-124">NOTES</span></span>

## <span data-ttu-id="36b13-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36b13-125">RELATED LINKS</span></span>

[<span data-ttu-id="36b13-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="36b13-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


