---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 06bdb5246cc0830ef78baa81d418f1fe6e51e935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968288"
---
# <span data-ttu-id="e1ccd-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ccd-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e1ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ccd-103">ANF(Azure NetApp Files) 스냅숏 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="e1ccd-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1ccd-104">SYNTAX</span></span>

### <span data-ttu-id="e1ccd-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1ccd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ccd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ccd-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ccd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ccd-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ccd-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ccd-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ccd-109">설명</span><span class="sxs-lookup"><span data-stu-id="e1ccd-109">DESCRIPTION</span></span>
<span data-ttu-id="e1ccd-110">**Remove-AzNetAppFilesSnapshotPolicy** cmdlet은 ANF 스냅숏 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="e1ccd-111">예제</span><span class="sxs-lookup"><span data-stu-id="e1ccd-111">EXAMPLES</span></span>

### <span data-ttu-id="e1ccd-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1ccd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="e1ccd-113">이 명령은 "MyAccount"에 대해 "MyBackupPolicy"라는 이름으로 새 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="e1ccd-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1ccd-114">PARAMETERS</span></span>

### <span data-ttu-id="e1ccd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e1ccd-115">-AccountName</span></span>
<span data-ttu-id="e1ccd-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="e1ccd-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="e1ccd-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e1ccd-117">-AccountObject</span></span>
<span data-ttu-id="e1ccd-118">새 스냅숏 정책 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="e1ccd-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="e1ccd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ccd-119">-DefaultProfile</span></span>
<span data-ttu-id="e1ccd-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ccd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1ccd-121">-InputObject</span></span>
<span data-ttu-id="e1ccd-122">제거할 SnapshotPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="e1ccd-122">The SnapshotPolicy object to remove</span></span>

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

### <span data-ttu-id="e1ccd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e1ccd-123">-Name</span></span>
<span data-ttu-id="e1ccd-124">ANF 스냅숏 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="e1ccd-124">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="e1ccd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1ccd-125">-PassThru</span></span>
<span data-ttu-id="e1ccd-126">지정된 계정이 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="e1ccd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ccd-127">-ResourceGroupName</span></span>
<span data-ttu-id="e1ccd-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="e1ccd-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e1ccd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1ccd-129">-ResourceId</span></span>
<span data-ttu-id="e1ccd-130">ANF 스냅숏 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e1ccd-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="e1ccd-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e1ccd-131">-Confirm</span></span>
<span data-ttu-id="e1ccd-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ccd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ccd-133">-WhatIf</span></span>
<span data-ttu-id="e1ccd-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ccd-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ccd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ccd-136">CommonParameters</span></span>
<span data-ttu-id="e1ccd-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1ccd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ccd-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1ccd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ccd-139">입력</span><span class="sxs-lookup"><span data-stu-id="e1ccd-139">INPUTS</span></span>

### <span data-ttu-id="e1ccd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e1ccd-140">System.String</span></span>

### <span data-ttu-id="e1ccd-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e1ccd-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e1ccd-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ccd-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e1ccd-143">출력</span><span class="sxs-lookup"><span data-stu-id="e1ccd-143">OUTPUTS</span></span>

### <span data-ttu-id="e1ccd-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e1ccd-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e1ccd-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1ccd-145">NOTES</span></span>

## <span data-ttu-id="e1ccd-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1ccd-146">RELATED LINKS</span></span>
