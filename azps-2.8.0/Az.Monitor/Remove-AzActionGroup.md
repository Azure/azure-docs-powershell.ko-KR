---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: c026d161c0d5a3ac73d2736d19422ce45b59fbd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871006"
---
# <span data-ttu-id="110a2-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="110a2-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="110a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="110a2-102">SYNOPSIS</span></span>
<span data-ttu-id="110a2-103">작업 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-103">Removes an action group.</span></span>

## <span data-ttu-id="110a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="110a2-104">SYNTAX</span></span>

### <span data-ttu-id="110a2-105">ByPropertyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="110a2-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110a2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="110a2-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="110a2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="110a2-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="110a2-108">DESCRIPTION</span></span>
<span data-ttu-id="110a2-109">**제거-AzActionGroup** cmdlet은 작업 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="110a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="110a2-110">EXAMPLES</span></span>

### <span data-ttu-id="110a2-111">예제 1: 작업 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="110a2-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="110a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="110a2-112">PARAMETERS</span></span>

### <span data-ttu-id="110a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110a2-113">-DefaultProfile</span></span>
<span data-ttu-id="110a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="110a2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="110a2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="110a2-115">-InputObject</span></span>
<span data-ttu-id="110a2-116">작업 그룹 리소스</span><span class="sxs-lookup"><span data-stu-id="110a2-116">The action group resource</span></span>

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

### <span data-ttu-id="110a2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="110a2-117">-Name</span></span>
<span data-ttu-id="110a2-118">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-118">The name of the action group.</span></span>

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

### <span data-ttu-id="110a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="110a2-120">자원 그룹 베트남</span><span class="sxs-lookup"><span data-stu-id="110a2-120">The resource group nam</span></span>

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

### <span data-ttu-id="110a2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="110a2-121">-ResourceId</span></span>
<span data-ttu-id="110a2-122">리소스 i</span><span class="sxs-lookup"><span data-stu-id="110a2-122">The resource i</span></span>

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

### <span data-ttu-id="110a2-123">-확인</span><span class="sxs-lookup"><span data-stu-id="110a2-123">-Confirm</span></span>
<span data-ttu-id="110a2-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="110a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="110a2-125">-WhatIf</span></span>
<span data-ttu-id="110a2-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="110a2-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="110a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110a2-128">CommonParameters</span></span>
<span data-ttu-id="110a2-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="110a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110a2-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="110a2-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110a2-131">입력</span><span class="sxs-lookup"><span data-stu-id="110a2-131">INPUTS</span></span>

### <span data-ttu-id="110a2-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="110a2-132">System.String</span></span>

### <span data-ttu-id="110a2-133">. Psactiongrou보도 정보 클래스.</span><span class="sxs-lookup"><span data-stu-id="110a2-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="110a2-134">출력</span><span class="sxs-lookup"><span data-stu-id="110a2-134">OUTPUTS</span></span>

### <span data-ttu-id="110a2-135">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="110a2-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="110a2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="110a2-136">NOTES</span></span>

## <span data-ttu-id="110a2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="110a2-137">RELATED LINKS</span></span>

<span data-ttu-id="110a2-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [새로운 AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="110a2-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
