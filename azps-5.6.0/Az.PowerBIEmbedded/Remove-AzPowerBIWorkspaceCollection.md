---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 1623b706a3878b517680782462e07ebacce2daf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953440"
---
# <span data-ttu-id="65215-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="65215-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="65215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65215-102">SYNOPSIS</span></span>
<span data-ttu-id="65215-103">Power BI 작업 영역 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="65215-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="65215-104">구문</span><span class="sxs-lookup"><span data-stu-id="65215-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65215-105">설명</span><span class="sxs-lookup"><span data-stu-id="65215-105">DESCRIPTION</span></span>
<span data-ttu-id="65215-106">**Remove-AzPowerBIWorkspaceCollection** cmdlet은 Azure 구독 및 리소스 그룹에서 Power BI 작업 영역 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="65215-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="65215-107">예제</span><span class="sxs-lookup"><span data-stu-id="65215-107">EXAMPLES</span></span>

### <span data-ttu-id="65215-108">예제 1: 작업 영역 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="65215-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="65215-109">이 명령은 지정된 리소스 그룹에서 WCN11이라는 작업 영역 컬렉션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="65215-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="65215-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65215-110">PARAMETERS</span></span>

### <span data-ttu-id="65215-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65215-111">-DefaultProfile</span></span>
<span data-ttu-id="65215-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65215-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65215-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65215-113">-ResourceGroupName</span></span>
<span data-ttu-id="65215-114">이 cmdlet에서 작업 영역 컬렉션을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65215-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="65215-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="65215-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="65215-116">이 cmdlet에서 제거한 Power BI 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65215-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="65215-117">-확인</span><span class="sxs-lookup"><span data-stu-id="65215-117">-Confirm</span></span>
<span data-ttu-id="65215-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65215-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65215-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65215-119">-WhatIf</span></span>
<span data-ttu-id="65215-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65215-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65215-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65215-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65215-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65215-122">CommonParameters</span></span>
<span data-ttu-id="65215-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65215-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65215-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="65215-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65215-125">입력</span><span class="sxs-lookup"><span data-stu-id="65215-125">INPUTS</span></span>

### <span data-ttu-id="65215-126">System.String</span><span class="sxs-lookup"><span data-stu-id="65215-126">System.String</span></span>

## <span data-ttu-id="65215-127">출력</span><span class="sxs-lookup"><span data-stu-id="65215-127">OUTPUTS</span></span>

### <span data-ttu-id="65215-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="65215-128">System.Void</span></span>

## <span data-ttu-id="65215-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65215-129">NOTES</span></span>

## <span data-ttu-id="65215-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65215-130">RELATED LINKS</span></span>

[<span data-ttu-id="65215-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="65215-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="65215-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="65215-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


