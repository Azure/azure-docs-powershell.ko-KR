---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213208"
---
# <span data-ttu-id="51458-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="51458-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="51458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51458-102">SYNOPSIS</span></span>
<span data-ttu-id="51458-103">장치에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51458-103">Removes a user on a device.</span></span>

## <span data-ttu-id="51458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51458-104">SYNTAX</span></span>

### <span data-ttu-id="51458-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="51458-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51458-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51458-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51458-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51458-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51458-108">설명은</span><span class="sxs-lookup"><span data-stu-id="51458-108">DESCRIPTION</span></span>
<span data-ttu-id="51458-109">**AzStackEdgeUser** Cmdlet은 스택 가장자리 장치에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="51458-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="51458-110">유형의 사용자 만들기만 `Share` 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51458-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="51458-111">예제의</span><span class="sxs-lookup"><span data-stu-id="51458-111">EXAMPLES</span></span>

### <span data-ttu-id="51458-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="51458-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="51458-113">변수</span><span class="sxs-lookup"><span data-stu-id="51458-113">PARAMETERS</span></span>

### <span data-ttu-id="51458-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51458-114">-AsJob</span></span>
<span data-ttu-id="51458-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="51458-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51458-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51458-116">-DefaultProfile</span></span>
<span data-ttu-id="51458-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51458-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51458-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="51458-118">-DeviceName</span></span>
<span data-ttu-id="51458-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="51458-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51458-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51458-120">-InputObject</span></span>
<span data-ttu-id="51458-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="51458-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51458-122">-이름</span><span class="sxs-lookup"><span data-stu-id="51458-122">-Name</span></span>
<span data-ttu-id="51458-123">사용자</span><span class="sxs-lookup"><span data-stu-id="51458-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51458-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51458-124">-PassThru</span></span>
<span data-ttu-id="51458-125">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="51458-125">returns true if successful</span></span>

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

### <span data-ttu-id="51458-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51458-126">-ResourceGroupName</span></span>
<span data-ttu-id="51458-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="51458-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51458-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51458-128">-ResourceId</span></span>
<span data-ttu-id="51458-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="51458-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51458-130">-확인</span><span class="sxs-lookup"><span data-stu-id="51458-130">-Confirm</span></span>
<span data-ttu-id="51458-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="51458-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51458-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51458-132">-WhatIf</span></span>
<span data-ttu-id="51458-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51458-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51458-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51458-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51458-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51458-135">CommonParameters</span></span>
<span data-ttu-id="51458-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51458-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51458-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51458-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51458-138">입력</span><span class="sxs-lookup"><span data-stu-id="51458-138">INPUTS</span></span>

### <span data-ttu-id="51458-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="51458-139">System.String</span></span>

### <span data-ttu-id="51458-140">StackEdge. PSStackEdgeUser에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="51458-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="51458-141">출력</span><span class="sxs-lookup"><span data-stu-id="51458-141">OUTPUTS</span></span>

### <span data-ttu-id="51458-142">StackEdge. PSStackEdgeStorageAccountCredential에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="51458-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="51458-143">상속자</span><span class="sxs-lookup"><span data-stu-id="51458-143">NOTES</span></span>

## <span data-ttu-id="51458-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51458-144">RELATED LINKS</span></span>
