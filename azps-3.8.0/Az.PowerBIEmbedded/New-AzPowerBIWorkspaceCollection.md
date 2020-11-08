---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034086"
---
# <span data-ttu-id="ed28f-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ed28f-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="ed28f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed28f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed28f-103">Power BI 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="ed28f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed28f-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed28f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed28f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed28f-106">**AzPowerBIWorkspaceCollection** cmdlet은 지정 된 리소스 그룹 및 위치에서 Azure 구독에 대 한 Power BI 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="ed28f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ed28f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed28f-108">예제 1: 작업 영역 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="ed28f-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="ed28f-109">이 명령은 지정 된 위치에 지정 된 리소스 그룹에 WCN11 이라는 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="ed28f-110">변수</span><span class="sxs-lookup"><span data-stu-id="ed28f-110">PARAMETERS</span></span>

### <span data-ttu-id="ed28f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed28f-111">-DefaultProfile</span></span>
<span data-ttu-id="ed28f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ed28f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed28f-113">-위치</span><span class="sxs-lookup"><span data-stu-id="ed28f-113">-Location</span></span>
<span data-ttu-id="ed28f-114">이 cmdlet이 작업 영역 컬렉션을 만드는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed28f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed28f-115">-ResourceGroupName</span></span>
<span data-ttu-id="ed28f-116">이 cmdlet이 작업 영역 컬렉션을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="ed28f-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="ed28f-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="ed28f-118">Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="ed28f-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ed28f-119">-Confirm</span></span>
<span data-ttu-id="ed28f-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed28f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed28f-121">-WhatIf</span></span>
<span data-ttu-id="ed28f-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed28f-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed28f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed28f-124">CommonParameters</span></span>
<span data-ttu-id="ed28f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed28f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed28f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed28f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed28f-127">입력</span><span class="sxs-lookup"><span data-stu-id="ed28f-127">INPUTS</span></span>

### <span data-ttu-id="ed28f-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed28f-128">System.String</span></span>

## <span data-ttu-id="ed28f-129">출력</span><span class="sxs-lookup"><span data-stu-id="ed28f-129">OUTPUTS</span></span>

### <span data-ttu-id="ed28f-130">PSWorkspaceCollection. PowerBIEmbedded. \*.</span><span class="sxs-lookup"><span data-stu-id="ed28f-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="ed28f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ed28f-131">NOTES</span></span>

## <span data-ttu-id="ed28f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed28f-132">RELATED LINKS</span></span>

[<span data-ttu-id="ed28f-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ed28f-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="ed28f-134">제거-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ed28f-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


