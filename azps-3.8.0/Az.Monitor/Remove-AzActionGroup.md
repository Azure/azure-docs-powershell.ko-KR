---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 06d744f5c36340c3c5297c3bd4ce22f1585e8bce
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412064"
---
# <span data-ttu-id="42c30-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="42c30-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="42c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c30-102">SYNOPSIS</span></span>
<span data-ttu-id="42c30-103">작업 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="42c30-103">Removes an action group.</span></span>

## <span data-ttu-id="42c30-104">구문</span><span class="sxs-lookup"><span data-stu-id="42c30-104">SYNTAX</span></span>

### <span data-ttu-id="42c30-105">ByPropertyName(기본값)</span><span class="sxs-lookup"><span data-stu-id="42c30-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c30-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42c30-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42c30-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42c30-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c30-108">설명</span><span class="sxs-lookup"><span data-stu-id="42c30-108">DESCRIPTION</span></span>
<span data-ttu-id="42c30-109">**Remove-AzActionGroup** cmdlet은 작업 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="42c30-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="42c30-110">예제</span><span class="sxs-lookup"><span data-stu-id="42c30-110">EXAMPLES</span></span>

### <span data-ttu-id="42c30-111">예제 1: 작업 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="42c30-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="42c30-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42c30-112">PARAMETERS</span></span>

### <span data-ttu-id="42c30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c30-113">-DefaultProfile</span></span>
<span data-ttu-id="42c30-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="42c30-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42c30-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42c30-115">-InputObject</span></span>
<span data-ttu-id="42c30-116">작업 그룹 리소스</span><span class="sxs-lookup"><span data-stu-id="42c30-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c30-117">-Name</span><span class="sxs-lookup"><span data-stu-id="42c30-117">-Name</span></span>
<span data-ttu-id="42c30-118">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42c30-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c30-119">-ResourceGroupName</span></span>
<span data-ttu-id="42c30-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="42c30-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c30-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42c30-121">-ResourceId</span></span>
<span data-ttu-id="42c30-122">리소스 i</span><span class="sxs-lookup"><span data-stu-id="42c30-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c30-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42c30-123">-Confirm</span></span>
<span data-ttu-id="42c30-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42c30-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c30-125">-WhatIf</span></span>
<span data-ttu-id="42c30-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="42c30-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42c30-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42c30-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c30-128">CommonParameters</span></span>
<span data-ttu-id="42c30-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42c30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c30-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42c30-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c30-131">입력</span><span class="sxs-lookup"><span data-stu-id="42c30-131">INPUTS</span></span>

### <span data-ttu-id="42c30-132">System.String</span><span class="sxs-lookup"><span data-stu-id="42c30-132">System.String</span></span>

### <span data-ttu-id="42c30-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="42c30-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="42c30-134">출력</span><span class="sxs-lookup"><span data-stu-id="42c30-134">OUTPUTS</span></span>

### <span data-ttu-id="42c30-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="42c30-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="42c30-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42c30-136">NOTES</span></span>

## <span data-ttu-id="42c30-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42c30-137">RELATED LINKS</span></span>

<span data-ttu-id="42c30-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="42c30-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)</span></span>

