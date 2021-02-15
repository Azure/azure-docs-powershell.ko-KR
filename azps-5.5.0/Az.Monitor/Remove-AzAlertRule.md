---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207128"
---
# <span data-ttu-id="1950f-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="1950f-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="1950f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1950f-102">SYNOPSIS</span></span>
<span data-ttu-id="1950f-103">경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-103">Removes an alert rule.</span></span>

## <span data-ttu-id="1950f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1950f-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1950f-105">설명</span><span class="sxs-lookup"><span data-stu-id="1950f-105">DESCRIPTION</span></span>
<span data-ttu-id="1950f-106">**Remove-AzAlertRule** cmdlet은 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="1950f-107">경고 규칙의 이름과 경고 규칙이 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="1950f-108">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1950f-109">예제</span><span class="sxs-lookup"><span data-stu-id="1950f-109">EXAMPLES</span></span>

### <span data-ttu-id="1950f-110">예제 1: 경고 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="1950f-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="1950f-111">이 명령은 리소스 그룹 Default-Web-CentralUS에서 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8이라는 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="1950f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1950f-112">PARAMETERS</span></span>

### <span data-ttu-id="1950f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1950f-113">-DefaultProfile</span></span>
<span data-ttu-id="1950f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1950f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1950f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1950f-115">-Name</span></span>
<span data-ttu-id="1950f-116">제거할 경고 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1950f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1950f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1950f-118">경고 규칙에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1950f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1950f-119">-Confirm</span></span>
<span data-ttu-id="1950f-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1950f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1950f-121">-WhatIf</span></span>
<span data-ttu-id="1950f-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1950f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1950f-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1950f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1950f-124">CommonParameters</span></span>
<span data-ttu-id="1950f-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1950f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1950f-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1950f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1950f-127">입력</span><span class="sxs-lookup"><span data-stu-id="1950f-127">INPUTS</span></span>

### <span data-ttu-id="1950f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1950f-128">System.String</span></span>

## <span data-ttu-id="1950f-129">출력</span><span class="sxs-lookup"><span data-stu-id="1950f-129">OUTPUTS</span></span>

### <span data-ttu-id="1950f-130">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1950f-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1950f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1950f-131">NOTES</span></span>

## <span data-ttu-id="1950f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1950f-132">RELATED LINKS</span></span>

[<span data-ttu-id="1950f-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="1950f-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="1950f-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="1950f-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="1950f-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="1950f-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="1950f-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="1950f-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


