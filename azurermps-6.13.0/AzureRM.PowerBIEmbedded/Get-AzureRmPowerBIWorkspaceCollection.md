---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7d7fefad86534cd2614312b21bd3ac392050e1b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529437"
---
# <span data-ttu-id="a2dc9-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a2dc9-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="a2dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dc9-103">Power BI 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2dc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2dc9-104">SYNTAX</span></span>

### <span data-ttu-id="a2dc9-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2dc9-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2dc9-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2dc9-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2dc9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a2dc9-107">DESCRIPTION</span></span>
<span data-ttu-id="a2dc9-108">**AzureRmPowerBIWorkspaceCollection** Cmdlet은 Azure 구독, 리소스 그룹 또는 컬렉션 이름에서 Power BI 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="a2dc9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a2dc9-109">EXAMPLES</span></span>

### <span data-ttu-id="a2dc9-110">예제 1: 리소스 그룹의 모든 작업 영역 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="a2dc9-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="a2dc9-111">이 명령은 ResourceGroup17 이라는 리소스 그룹에 속하는 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="a2dc9-112">예제 2: 이름을 사용 하 여 작업 영역 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="a2dc9-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="a2dc9-113">이 명령은 지정 된 리소스 그룹에서 WCN11 이라는 작업 영역 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="a2dc9-114">변수</span><span class="sxs-lookup"><span data-stu-id="a2dc9-114">PARAMETERS</span></span>

### <span data-ttu-id="a2dc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2dc9-115">-DefaultProfile</span></span>
<span data-ttu-id="a2dc9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2dc9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2dc9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2dc9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2dc9-118">이 cmdlet이 작업 영역 컬렉션을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="a2dc9-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a2dc9-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a2dc9-120">이 cmdlet이 가져오는 Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a2dc9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dc9-121">CommonParameters</span></span>
<span data-ttu-id="a2dc9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dc9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2dc9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dc9-124">입력</span><span class="sxs-lookup"><span data-stu-id="a2dc9-124">INPUTS</span></span>

### <span data-ttu-id="a2dc9-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2dc9-125">System.String</span></span>

## <span data-ttu-id="a2dc9-126">출력</span><span class="sxs-lookup"><span data-stu-id="a2dc9-126">OUTPUTS</span></span>

### <span data-ttu-id="a2dc9-127">PSWorkspaceCollection. PowerBIEmbedded. \*.</span><span class="sxs-lookup"><span data-stu-id="a2dc9-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="a2dc9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="a2dc9-128">NOTES</span></span>

## <span data-ttu-id="a2dc9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2dc9-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2dc9-130">새로운 AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a2dc9-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="a2dc9-131">제거-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a2dc9-131">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


