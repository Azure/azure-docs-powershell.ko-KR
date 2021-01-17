---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359822"
---
# <span data-ttu-id="ff76d-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ff76d-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="ff76d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff76d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff76d-103">ANF(Azure NetApp Files) 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="ff76d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff76d-104">SYNTAX</span></span>

### <span data-ttu-id="ff76d-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff76d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff76d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff76d-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff76d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff76d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff76d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff76d-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff76d-109">설명</span><span class="sxs-lookup"><span data-stu-id="ff76d-109">DESCRIPTION</span></span>
<span data-ttu-id="ff76d-110">**Remove-AzNetAppFilesPool** cmdlet은 ANF 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="ff76d-111">예제</span><span class="sxs-lookup"><span data-stu-id="ff76d-111">EXAMPLES</span></span>

### <span data-ttu-id="ff76d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff76d-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="ff76d-113">이 명령은 ANF 풀 "MyAnfPool"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="ff76d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff76d-114">PARAMETERS</span></span>

### <span data-ttu-id="ff76d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff76d-115">-AccountName</span></span>
<span data-ttu-id="ff76d-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="ff76d-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ff76d-117">-AccountObject</span></span>
<span data-ttu-id="ff76d-118">제거할 풀이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ff76d-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff76d-119">-DefaultProfile</span></span>
<span data-ttu-id="ff76d-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff76d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff76d-121">-InputObject</span></span>
<span data-ttu-id="ff76d-122">제거할 풀 개체</span><span class="sxs-lookup"><span data-stu-id="ff76d-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ff76d-123">-Name</span></span>
<span data-ttu-id="ff76d-124">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="ff76d-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff76d-125">-PassThru</span></span>
<span data-ttu-id="ff76d-126">지정된 풀이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="ff76d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff76d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff76d-128">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ff76d-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff76d-129">-ResourceId</span></span>
<span data-ttu-id="ff76d-130">ANF 풀의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ff76d-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff76d-131">-Confirm</span></span>
<span data-ttu-id="ff76d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff76d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff76d-133">-WhatIf</span></span>
<span data-ttu-id="ff76d-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff76d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff76d-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff76d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff76d-136">CommonParameters</span></span>
<span data-ttu-id="ff76d-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff76d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff76d-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff76d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff76d-139">입력</span><span class="sxs-lookup"><span data-stu-id="ff76d-139">INPUTS</span></span>

### <span data-ttu-id="ff76d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ff76d-140">System.String</span></span>

### <span data-ttu-id="ff76d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ff76d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ff76d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ff76d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ff76d-143">출력</span><span class="sxs-lookup"><span data-stu-id="ff76d-143">OUTPUTS</span></span>

### <span data-ttu-id="ff76d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff76d-144">System.Boolean</span></span>

## <span data-ttu-id="ff76d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff76d-145">NOTES</span></span>

## <span data-ttu-id="ff76d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff76d-146">RELATED LINKS</span></span>
