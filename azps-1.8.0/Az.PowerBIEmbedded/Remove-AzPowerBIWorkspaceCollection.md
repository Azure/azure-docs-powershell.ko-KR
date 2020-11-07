---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 058a914540cd03bcf523f0300e18299c3cf084ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699804"
---
# <span data-ttu-id="259ad-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="259ad-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="259ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="259ad-102">SYNOPSIS</span></span>
<span data-ttu-id="259ad-103">Power BI 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="259ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="259ad-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="259ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="259ad-105">DESCRIPTION</span></span>
<span data-ttu-id="259ad-106">**AzPowerBIWorkspaceCollection** Cmdlet은 Azure 구독 및 리소스 그룹에서 Power BI 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="259ad-107">예제의</span><span class="sxs-lookup"><span data-stu-id="259ad-107">EXAMPLES</span></span>

### <span data-ttu-id="259ad-108">예제 1: 작업 영역 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="259ad-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="259ad-109">이 명령은 지정 된 리소스 그룹에서 WCN11 이라는 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="259ad-110">변수</span><span class="sxs-lookup"><span data-stu-id="259ad-110">PARAMETERS</span></span>

### <span data-ttu-id="259ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259ad-111">-DefaultProfile</span></span>
<span data-ttu-id="259ad-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="259ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="259ad-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259ad-113">-ResourceGroupName</span></span>
<span data-ttu-id="259ad-114">이 cmdlet이 작업 영역 컬렉션을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="259ad-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="259ad-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="259ad-116">이 cmdlet이 제거 하는 Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="259ad-117">-확인</span><span class="sxs-lookup"><span data-stu-id="259ad-117">-Confirm</span></span>
<span data-ttu-id="259ad-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259ad-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259ad-119">-WhatIf</span></span>
<span data-ttu-id="259ad-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259ad-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259ad-122">CommonParameters</span></span>
<span data-ttu-id="259ad-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="259ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259ad-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259ad-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259ad-125">입력</span><span class="sxs-lookup"><span data-stu-id="259ad-125">INPUTS</span></span>

### <span data-ttu-id="259ad-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="259ad-126">System.String</span></span>

## <span data-ttu-id="259ad-127">출력</span><span class="sxs-lookup"><span data-stu-id="259ad-127">OUTPUTS</span></span>

### <span data-ttu-id="259ad-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="259ad-128">System.Void</span></span>

## <span data-ttu-id="259ad-129">상속자</span><span class="sxs-lookup"><span data-stu-id="259ad-129">NOTES</span></span>

## <span data-ttu-id="259ad-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="259ad-130">RELATED LINKS</span></span>

[<span data-ttu-id="259ad-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="259ad-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="259ad-132">새로운 AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="259ad-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


