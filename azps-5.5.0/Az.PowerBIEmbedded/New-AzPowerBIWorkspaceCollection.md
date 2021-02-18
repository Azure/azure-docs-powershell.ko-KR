---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202140"
---
# <span data-ttu-id="31180-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="31180-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="31180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31180-102">SYNOPSIS</span></span>
<span data-ttu-id="31180-103">Power BI 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31180-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="31180-104">구문</span><span class="sxs-lookup"><span data-stu-id="31180-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31180-105">설명</span><span class="sxs-lookup"><span data-stu-id="31180-105">DESCRIPTION</span></span>
<span data-ttu-id="31180-106">**New-AzPowerBIWorkspaceCollection** cmdlet은 지정된 리소스 그룹 및 위치에 Azure 구독에 대한 Power BI 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31180-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="31180-107">예제</span><span class="sxs-lookup"><span data-stu-id="31180-107">EXAMPLES</span></span>

### <span data-ttu-id="31180-108">예제 1: 작업 영역 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="31180-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="31180-109">이 명령은 지정된 위치의 지정된 리소스 그룹에 WCN11이라는 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31180-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="31180-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31180-110">PARAMETERS</span></span>

### <span data-ttu-id="31180-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31180-111">-DefaultProfile</span></span>
<span data-ttu-id="31180-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31180-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31180-113">-Location</span><span class="sxs-lookup"><span data-stu-id="31180-113">-Location</span></span>
<span data-ttu-id="31180-114">이 cmdlet이 작업 영역 컬렉션을 만드는 Azure 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31180-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="31180-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31180-115">-ResourceGroupName</span></span>
<span data-ttu-id="31180-116">이 cmdlet이 작업 영역 컬렉션을 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31180-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="31180-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="31180-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="31180-118">Power BI 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31180-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="31180-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31180-119">-Confirm</span></span>
<span data-ttu-id="31180-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31180-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31180-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31180-121">-WhatIf</span></span>
<span data-ttu-id="31180-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="31180-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31180-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31180-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31180-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31180-124">CommonParameters</span></span>
<span data-ttu-id="31180-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31180-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31180-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31180-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31180-127">입력</span><span class="sxs-lookup"><span data-stu-id="31180-127">INPUTS</span></span>

### <span data-ttu-id="31180-128">System.String</span><span class="sxs-lookup"><span data-stu-id="31180-128">System.String</span></span>

## <span data-ttu-id="31180-129">출력</span><span class="sxs-lookup"><span data-stu-id="31180-129">OUTPUTS</span></span>

### <span data-ttu-id="31180-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="31180-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="31180-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31180-131">NOTES</span></span>

## <span data-ttu-id="31180-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31180-132">RELATED LINKS</span></span>

[<span data-ttu-id="31180-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="31180-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="31180-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="31180-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


