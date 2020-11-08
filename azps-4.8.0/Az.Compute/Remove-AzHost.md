---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049115"
---
# <span data-ttu-id="2fb0e-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2fb0e-101">Remove-AzHost</span></span>

## <span data-ttu-id="2fb0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb0e-103">호스트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-103">Removes a host.</span></span>

## <span data-ttu-id="2fb0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fb0e-104">SYNTAX</span></span>

### <span data-ttu-id="2fb0e-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="2fb0e-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fb0e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2fb0e-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fb0e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2fb0e-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fb0e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2fb0e-108">DESCRIPTION</span></span>
<span data-ttu-id="2fb0e-109">이 cmdlet은 호스트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="2fb0e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2fb0e-110">EXAMPLES</span></span>

### <span data-ttu-id="2fb0e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2fb0e-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="2fb0e-112">이 명령은 지정 된 호스트를 가져오고 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="2fb0e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2fb0e-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="2fb0e-114">이 명령은 지정 된 호스트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-114">This command removes the given host.</span></span>

## <span data-ttu-id="2fb0e-115">변수</span><span class="sxs-lookup"><span data-stu-id="2fb0e-115">PARAMETERS</span></span>

### <span data-ttu-id="2fb0e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fb0e-116">-AsJob</span></span>
<span data-ttu-id="2fb0e-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2fb0e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fb0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb0e-118">-DefaultProfile</span></span>
<span data-ttu-id="2fb0e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fb0e-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb0e-120">-HostGroupName</span></span>
<span data-ttu-id="2fb0e-121">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb0e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fb0e-122">-InputObject</span></span>
<span data-ttu-id="2fb0e-123">호스트의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb0e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="2fb0e-124">-Name</span></span>
<span data-ttu-id="2fb0e-125">호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb0e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb0e-126">-ResourceGroupName</span></span>
<span data-ttu-id="2fb0e-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb0e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fb0e-128">-ResourceId</span></span>
<span data-ttu-id="2fb0e-129">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb0e-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2fb0e-130">-Confirm</span></span>
<span data-ttu-id="2fb0e-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb0e-132">-WhatIf</span></span>
<span data-ttu-id="2fb0e-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb0e-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb0e-135">CommonParameters</span></span>
<span data-ttu-id="2fb0e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb0e-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb0e-138">입력</span><span class="sxs-lookup"><span data-stu-id="2fb0e-138">INPUTS</span></span>

### <span data-ttu-id="2fb0e-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2fb0e-139">System.String</span></span>

### <span data-ttu-id="2fb0e-140">PSHost의. m a.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="2fb0e-141">출력</span><span class="sxs-lookup"><span data-stu-id="2fb0e-141">OUTPUTS</span></span>

### <span data-ttu-id="2fb0e-142">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="2fb0e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2fb0e-143">상속자</span><span class="sxs-lookup"><span data-stu-id="2fb0e-143">NOTES</span></span>

## <span data-ttu-id="2fb0e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fb0e-144">RELATED LINKS</span></span>
