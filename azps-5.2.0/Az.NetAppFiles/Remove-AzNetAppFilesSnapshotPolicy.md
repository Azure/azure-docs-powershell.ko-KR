---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325926"
---
# <span data-ttu-id="e87c3-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e87c3-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e87c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e87c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e87c3-103">ANF(Azure NetApp Files) 스냅숏 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="e87c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e87c3-104">SYNTAX</span></span>

### <span data-ttu-id="e87c3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e87c3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e87c3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87c3-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e87c3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87c3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e87c3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87c3-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87c3-109">설명</span><span class="sxs-lookup"><span data-stu-id="e87c3-109">DESCRIPTION</span></span>
<span data-ttu-id="e87c3-110">**Remove-AzNetAppFilesSnapshotPolicy** cmdlet은 ANF 스냅숏 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="e87c3-111">예제</span><span class="sxs-lookup"><span data-stu-id="e87c3-111">EXAMPLES</span></span>

### <span data-ttu-id="e87c3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e87c3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="e87c3-113">이 명령은 "MyAccount" 계정에 대해 이름이 "MyBackupPolicy"인 새 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="e87c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e87c3-114">PARAMETERS</span></span>

### <span data-ttu-id="e87c3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e87c3-115">-AccountName</span></span>
<span data-ttu-id="e87c3-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="e87c3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="e87c3-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e87c3-117">-AccountObject</span></span>
<span data-ttu-id="e87c3-118">새 스냅숏 정책 개체의 계정</span><span class="sxs-lookup"><span data-stu-id="e87c3-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="e87c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87c3-119">-DefaultProfile</span></span>
<span data-ttu-id="e87c3-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e87c3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e87c3-121">-InputObject</span></span>
<span data-ttu-id="e87c3-122">제거할 SnapshotPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="e87c3-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e87c3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e87c3-123">-Name</span></span>
<span data-ttu-id="e87c3-124">ANF 스냅숏 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="e87c3-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87c3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e87c3-125">-PassThru</span></span>
<span data-ttu-id="e87c3-126">지정된 계정이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="e87c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e87c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="e87c3-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="e87c3-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e87c3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e87c3-129">-ResourceId</span></span>
<span data-ttu-id="e87c3-130">ANF 스냅숏 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e87c3-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="e87c3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e87c3-131">-Confirm</span></span>
<span data-ttu-id="e87c3-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87c3-133">-WhatIf</span></span>
<span data-ttu-id="e87c3-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e87c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e87c3-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87c3-136">CommonParameters</span></span>
<span data-ttu-id="e87c3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87c3-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e87c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87c3-139">입력</span><span class="sxs-lookup"><span data-stu-id="e87c3-139">INPUTS</span></span>

### <span data-ttu-id="e87c3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e87c3-140">System.String</span></span>

### <span data-ttu-id="e87c3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e87c3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e87c3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e87c3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e87c3-143">출력</span><span class="sxs-lookup"><span data-stu-id="e87c3-143">OUTPUTS</span></span>

### <span data-ttu-id="e87c3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e87c3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e87c3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e87c3-145">NOTES</span></span>

## <span data-ttu-id="e87c3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e87c3-146">RELATED LINKS</span></span>
