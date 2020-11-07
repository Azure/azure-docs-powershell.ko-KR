---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: aad8ebb5b78163319ca0c6f56780bd0e336853f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875717"
---
# <span data-ttu-id="6ed88-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="6ed88-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="6ed88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed88-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed88-103">새를 만들거나 기존 작업 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="6ed88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ed88-104">SYNTAX</span></span>

### <span data-ttu-id="6ed88-105">ByPropertyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ed88-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed88-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ed88-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed88-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6ed88-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ed88-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ed88-108">DESCRIPTION</span></span>
<span data-ttu-id="6ed88-109">**Set-AzActionGroup** cmdlet은 새 작업을 만들거나 기존 동작 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="6ed88-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ed88-110">EXAMPLES</span></span>

### <span data-ttu-id="6ed88-111">예제 1: 작업 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="6ed88-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="6ed88-112">처음 두 명령은 두 개의 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="6ed88-113">마지막 명령은 두 개의 수신기를 포함 하는 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="6ed88-114">변수</span><span class="sxs-lookup"><span data-stu-id="6ed88-114">PARAMETERS</span></span>

### <span data-ttu-id="6ed88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed88-115">-DefaultProfile</span></span>
<span data-ttu-id="6ed88-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6ed88-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ed88-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="6ed88-117">-DisableGroup</span></span>
<span data-ttu-id="6ed88-118">작업 그룹을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-118">Disables the action group.</span></span>

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

### <span data-ttu-id="6ed88-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ed88-119">-InputObject</span></span>
<span data-ttu-id="6ed88-120">작업 그룹 리소스</span><span class="sxs-lookup"><span data-stu-id="6ed88-120">The action group resource</span></span>

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

### <span data-ttu-id="6ed88-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6ed88-121">-Name</span></span>
<span data-ttu-id="6ed88-122">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-122">The name of the action group.</span></span>

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

### <span data-ttu-id="6ed88-123">-수신자</span><span class="sxs-lookup"><span data-stu-id="6ed88-123">-Receiver</span></span>
<span data-ttu-id="6ed88-124">작업 그룹의 수신기 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="6ed88-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed88-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ed88-126">자원 그룹 베트남</span><span class="sxs-lookup"><span data-stu-id="6ed88-126">The resource group nam</span></span>

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

### <span data-ttu-id="6ed88-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ed88-127">-ResourceId</span></span>
<span data-ttu-id="6ed88-128">리소스 i</span><span class="sxs-lookup"><span data-stu-id="6ed88-128">The resource i</span></span>

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

### <span data-ttu-id="6ed88-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="6ed88-129">-ShortName</span></span>
<span data-ttu-id="6ed88-130">작업 그룹의 약식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="6ed88-131">태그</span><span class="sxs-lookup"><span data-stu-id="6ed88-131">-Tag</span></span>
<span data-ttu-id="6ed88-132">작업 그룹 리소스의 태그</span><span class="sxs-lookup"><span data-stu-id="6ed88-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="6ed88-133">-확인</span><span class="sxs-lookup"><span data-stu-id="6ed88-133">-Confirm</span></span>
<span data-ttu-id="6ed88-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed88-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed88-135">-WhatIf</span></span>
<span data-ttu-id="6ed88-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ed88-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed88-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed88-138">CommonParameters</span></span>
<span data-ttu-id="6ed88-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed88-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed88-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ed88-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed88-141">입력</span><span class="sxs-lookup"><span data-stu-id="6ed88-141">INPUTS</span></span>

### <span data-ttu-id="6ed88-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ed88-142">System.String</span></span>

### <span data-ttu-id="6ed88-143">System.webserver. List ' 1 [[Microsoft Azure. PSActionGroupReceiverBase, Microsoft azure. PowerShell. a n t e. i = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ed88-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6ed88-144">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ed88-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6ed88-145">System.webserver. IDictionary ' 2 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e], [System.webserver, System.webserver. CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ed88-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ed88-146">. Psactiongrou보도 정보 클래스.</span><span class="sxs-lookup"><span data-stu-id="6ed88-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="6ed88-147">출력</span><span class="sxs-lookup"><span data-stu-id="6ed88-147">OUTPUTS</span></span>

### <span data-ttu-id="6ed88-148">. Psactiongrou보도 정보 클래스.</span><span class="sxs-lookup"><span data-stu-id="6ed88-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="6ed88-149">상속자</span><span class="sxs-lookup"><span data-stu-id="6ed88-149">NOTES</span></span>

## <span data-ttu-id="6ed88-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ed88-150">RELATED LINKS</span></span>

<span data-ttu-id="6ed88-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [제거-AzActionGroup](./Remove-AzActionGroup.md) 
 [새로운 AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="6ed88-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
