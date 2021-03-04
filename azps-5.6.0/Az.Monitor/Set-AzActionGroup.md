---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: 6c0843afa3001299a21f49cec5ed73f74bdcd2a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955819"
---
# <span data-ttu-id="81938-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="81938-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="81938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81938-102">SYNOPSIS</span></span>
<span data-ttu-id="81938-103">새 작업 그룹을 생성하거나 기존 작업 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="81938-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="81938-104">구문</span><span class="sxs-lookup"><span data-stu-id="81938-104">SYNTAX</span></span>

### <span data-ttu-id="81938-105">ByPropertyName(기본값)</span><span class="sxs-lookup"><span data-stu-id="81938-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81938-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81938-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81938-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81938-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81938-108">설명</span><span class="sxs-lookup"><span data-stu-id="81938-108">DESCRIPTION</span></span>
<span data-ttu-id="81938-109">**Set-AzActionGroup** cmdlet은 새 작업 그룹을 생성하거나 기존 작업 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="81938-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="81938-110">예제</span><span class="sxs-lookup"><span data-stu-id="81938-110">EXAMPLES</span></span>

### <span data-ttu-id="81938-111">예제 1: 작업 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="81938-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="81938-112">처음 두 명령은 두 개의 수신기를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="81938-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="81938-113">마지막 명령은 두 수신기를 포함하여 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81938-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="81938-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81938-114">PARAMETERS</span></span>

### <span data-ttu-id="81938-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81938-115">-DefaultProfile</span></span>
<span data-ttu-id="81938-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="81938-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81938-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="81938-117">-DisableGroup</span></span>
<span data-ttu-id="81938-118">작업 그룹을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="81938-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81938-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81938-119">-InputObject</span></span>
<span data-ttu-id="81938-120">작업 그룹 리소스</span><span class="sxs-lookup"><span data-stu-id="81938-120">The action group resource</span></span>

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

### <span data-ttu-id="81938-121">-Name</span><span class="sxs-lookup"><span data-stu-id="81938-121">-Name</span></span>
<span data-ttu-id="81938-122">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81938-122">The name of the action group.</span></span>

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

### <span data-ttu-id="81938-123">-수신기</span><span class="sxs-lookup"><span data-stu-id="81938-123">-Receiver</span></span>
<span data-ttu-id="81938-124">작업 그룹의 수신기 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="81938-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81938-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81938-125">-ResourceGroupName</span></span>
<span data-ttu-id="81938-126">리소스 그룹 nam</span><span class="sxs-lookup"><span data-stu-id="81938-126">The resource group nam</span></span>

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

### <span data-ttu-id="81938-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81938-127">-ResourceId</span></span>
<span data-ttu-id="81938-128">리소스 i</span><span class="sxs-lookup"><span data-stu-id="81938-128">The resource i</span></span>

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

### <span data-ttu-id="81938-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="81938-129">-ShortName</span></span>
<span data-ttu-id="81938-130">작업 그룹의 짧은 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81938-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81938-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="81938-131">-Tag</span></span>
<span data-ttu-id="81938-132">작업 그룹 리소스의 태그</span><span class="sxs-lookup"><span data-stu-id="81938-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81938-133">-확인</span><span class="sxs-lookup"><span data-stu-id="81938-133">-Confirm</span></span>
<span data-ttu-id="81938-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81938-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81938-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81938-135">-WhatIf</span></span>
<span data-ttu-id="81938-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="81938-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81938-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81938-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81938-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81938-138">CommonParameters</span></span>
<span data-ttu-id="81938-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81938-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81938-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81938-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81938-141">입력</span><span class="sxs-lookup"><span data-stu-id="81938-141">INPUTS</span></span>

### <span data-ttu-id="81938-142">System.String</span><span class="sxs-lookup"><span data-stu-id="81938-142">System.String</span></span>

### <span data-ttu-id="81938-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="81938-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="81938-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81938-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="81938-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea798e]]</span><span class="sxs-lookup"><span data-stu-id="81938-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="81938-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="81938-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="81938-147">출력</span><span class="sxs-lookup"><span data-stu-id="81938-147">OUTPUTS</span></span>

### <span data-ttu-id="81938-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="81938-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="81938-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81938-149">NOTES</span></span>

## <span data-ttu-id="81938-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81938-150">RELATED LINKS</span></span>

<span data-ttu-id="81938-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="81938-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
