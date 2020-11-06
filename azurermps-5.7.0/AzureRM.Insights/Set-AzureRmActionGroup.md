---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: b4f509d6ba688cab993f83cd0b094b3f8394d36f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526819"
---
# <span data-ttu-id="41ffb-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="41ffb-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="41ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="41ffb-103">새를 만들거나 기존 작업 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41ffb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41ffb-104">SYNTAX</span></span>

### <span data-ttu-id="41ffb-105">ByPropertyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="41ffb-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ffb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41ffb-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ffb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="41ffb-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41ffb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="41ffb-108">DESCRIPTION</span></span>
<span data-ttu-id="41ffb-109">**Set-AzureRmActionGroup** cmdlet은 새 작업을 만들거나 기존 동작 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="41ffb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="41ffb-110">EXAMPLES</span></span>

### <span data-ttu-id="41ffb-111">예제 1: 작업 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="41ffb-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="41ffb-112">처음 두 명령은 두 개의 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="41ffb-113">마지막 명령은 두 개의 수신기를 포함 하는 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="41ffb-114">변수</span><span class="sxs-lookup"><span data-stu-id="41ffb-114">PARAMETERS</span></span>

### <span data-ttu-id="41ffb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ffb-115">-DefaultProfile</span></span>
<span data-ttu-id="41ffb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="41ffb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="41ffb-117">-DisableGroup</span></span>
<span data-ttu-id="41ffb-118">작업 그룹을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-118">Disables the action group.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41ffb-119">-InputObject</span></span>
<span data-ttu-id="41ffb-120">작업 그룹 resourc</span><span class="sxs-lookup"><span data-stu-id="41ffb-120">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="41ffb-121">-Name</span></span>
<span data-ttu-id="41ffb-122">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-122">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-123">-수신자</span><span class="sxs-lookup"><span data-stu-id="41ffb-123">-Receiver</span></span>
<span data-ttu-id="41ffb-124">작업 그룹의 수신기 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="41ffb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ffb-125">-ResourceGroupName</span></span>
<span data-ttu-id="41ffb-126">자원 그룹 베트남</span><span class="sxs-lookup"><span data-stu-id="41ffb-126">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41ffb-127">-ResourceId</span></span>
<span data-ttu-id="41ffb-128">리소스 i</span><span class="sxs-lookup"><span data-stu-id="41ffb-128">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="41ffb-129">-ShortName</span></span>
<span data-ttu-id="41ffb-130">작업 그룹의 약식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-130">The short name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName, ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-131">태그</span><span class="sxs-lookup"><span data-stu-id="41ffb-131">-Tag</span></span>
<span data-ttu-id="41ffb-132">작업 그룹 resourc의 태그</span><span class="sxs-lookup"><span data-stu-id="41ffb-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="41ffb-133">-확인</span><span class="sxs-lookup"><span data-stu-id="41ffb-133">-Confirm</span></span>
<span data-ttu-id="41ffb-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ffb-135">-WhatIf</span></span>
<span data-ttu-id="41ffb-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41ffb-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ffb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ffb-138">CommonParameters</span></span>
<span data-ttu-id="41ffb-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ffb-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ffb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ffb-141">입력</span><span class="sxs-lookup"><span data-stu-id="41ffb-141">INPUTS</span></span>

### <span data-ttu-id="41ffb-142">않아야</span><span class="sxs-lookup"><span data-stu-id="41ffb-142">None</span></span>
<span data-ttu-id="41ffb-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41ffb-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41ffb-144">출력</span><span class="sxs-lookup"><span data-stu-id="41ffb-144">OUTPUTS</span></span>

### <span data-ttu-id="41ffb-145">. Psactiongrou보도 정보 클래스.</span><span class="sxs-lookup"><span data-stu-id="41ffb-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="41ffb-146">상속자</span><span class="sxs-lookup"><span data-stu-id="41ffb-146">NOTES</span></span>

## <span data-ttu-id="41ffb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41ffb-147">RELATED LINKS</span></span>

<span data-ttu-id="41ffb-148">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [제거-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [새로운 AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="41ffb-148">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
