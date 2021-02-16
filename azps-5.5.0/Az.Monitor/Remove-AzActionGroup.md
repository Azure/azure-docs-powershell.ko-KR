---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180116"
---
# <span data-ttu-id="ea853-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ea853-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="ea853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea853-102">SYNOPSIS</span></span>
<span data-ttu-id="ea853-103">작업 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ea853-103">Removes an action group.</span></span>

## <span data-ttu-id="ea853-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea853-104">SYNTAX</span></span>

### <span data-ttu-id="ea853-105">ByPropertyName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ea853-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea853-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea853-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea853-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea853-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea853-108">설명</span><span class="sxs-lookup"><span data-stu-id="ea853-108">DESCRIPTION</span></span>
<span data-ttu-id="ea853-109">**Remove-AzActionGroup** cmdlet은 작업 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ea853-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="ea853-110">예제</span><span class="sxs-lookup"><span data-stu-id="ea853-110">EXAMPLES</span></span>

### <span data-ttu-id="ea853-111">예제 1: 작업 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="ea853-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="ea853-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea853-112">PARAMETERS</span></span>

### <span data-ttu-id="ea853-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea853-113">-DefaultProfile</span></span>
<span data-ttu-id="ea853-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ea853-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea853-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea853-115">-InputObject</span></span>
<span data-ttu-id="ea853-116">작업 그룹 리소스</span><span class="sxs-lookup"><span data-stu-id="ea853-116">The action group resource</span></span>

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

### <span data-ttu-id="ea853-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ea853-117">-Name</span></span>
<span data-ttu-id="ea853-118">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea853-118">The name of the action group.</span></span>

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

### <span data-ttu-id="ea853-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea853-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea853-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ea853-120">The resource group nam</span></span>

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

### <span data-ttu-id="ea853-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea853-121">-ResourceId</span></span>
<span data-ttu-id="ea853-122">리소스 i</span><span class="sxs-lookup"><span data-stu-id="ea853-122">The resource i</span></span>

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

### <span data-ttu-id="ea853-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea853-123">-Confirm</span></span>
<span data-ttu-id="ea853-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea853-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea853-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea853-125">-WhatIf</span></span>
<span data-ttu-id="ea853-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ea853-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea853-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea853-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea853-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea853-128">CommonParameters</span></span>
<span data-ttu-id="ea853-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea853-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea853-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea853-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea853-131">입력</span><span class="sxs-lookup"><span data-stu-id="ea853-131">INPUTS</span></span>

### <span data-ttu-id="ea853-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ea853-132">System.String</span></span>

### <span data-ttu-id="ea853-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="ea853-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="ea853-134">출력</span><span class="sxs-lookup"><span data-stu-id="ea853-134">OUTPUTS</span></span>

### <span data-ttu-id="ea853-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ea853-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ea853-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea853-136">NOTES</span></span>

## <span data-ttu-id="ea853-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea853-137">RELATED LINKS</span></span>

<span data-ttu-id="ea853-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="ea853-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
