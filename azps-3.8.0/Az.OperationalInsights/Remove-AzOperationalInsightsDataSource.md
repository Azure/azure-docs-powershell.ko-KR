---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044526"
---
# <span data-ttu-id="51fe2-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="51fe2-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="51fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="51fe2-103">데이터 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-103">Deletes a data source.</span></span>

## <span data-ttu-id="51fe2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51fe2-104">SYNTAX</span></span>

### <span data-ttu-id="51fe2-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="51fe2-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51fe2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="51fe2-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51fe2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51fe2-107">DESCRIPTION</span></span>
<span data-ttu-id="51fe2-108">**제거-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="51fe2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51fe2-109">EXAMPLES</span></span>

## <span data-ttu-id="51fe2-110">변수</span><span class="sxs-lookup"><span data-stu-id="51fe2-110">PARAMETERS</span></span>

### <span data-ttu-id="51fe2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fe2-111">-DefaultProfile</span></span>
<span data-ttu-id="51fe2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="51fe2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51fe2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="51fe2-113">-Force</span></span>
<span data-ttu-id="51fe2-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fe2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="51fe2-115">-Name</span></span>
<span data-ttu-id="51fe2-116">삭제할 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fe2-117">-ResourceGroupName</span></span>
<span data-ttu-id="51fe2-118">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe2-119">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="51fe2-119">-Workspace</span></span>
<span data-ttu-id="51fe2-120">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe2-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51fe2-121">-WorkspaceName</span></span>
<span data-ttu-id="51fe2-122">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe2-123">-확인</span><span class="sxs-lookup"><span data-stu-id="51fe2-123">-Confirm</span></span>
<span data-ttu-id="51fe2-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51fe2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fe2-125">-WhatIf</span></span>
<span data-ttu-id="51fe2-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fe2-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51fe2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fe2-128">CommonParameters</span></span>
<span data-ttu-id="51fe2-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51fe2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fe2-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fe2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fe2-131">입력</span><span class="sxs-lookup"><span data-stu-id="51fe2-131">INPUTS</span></span>

### <span data-ttu-id="51fe2-132">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="51fe2-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="51fe2-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51fe2-133">System.String</span></span>

## <span data-ttu-id="51fe2-134">출력</span><span class="sxs-lookup"><span data-stu-id="51fe2-134">OUTPUTS</span></span>

### <span data-ttu-id="51fe2-135">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="51fe2-135">System.Void</span></span>

## <span data-ttu-id="51fe2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="51fe2-136">NOTES</span></span>
* <span data-ttu-id="51fe2-137">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="51fe2-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="51fe2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51fe2-138">RELATED LINKS</span></span>

[<span data-ttu-id="51fe2-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="51fe2-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="51fe2-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="51fe2-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


