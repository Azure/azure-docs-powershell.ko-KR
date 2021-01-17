---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492245"
---
# <span data-ttu-id="11746-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="11746-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="11746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11746-102">SYNOPSIS</span></span>
<span data-ttu-id="11746-103">ANF(Azure NetApp Files) 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="11746-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="11746-104">구문</span><span class="sxs-lookup"><span data-stu-id="11746-104">SYNTAX</span></span>

### <span data-ttu-id="11746-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="11746-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11746-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11746-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11746-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11746-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11746-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11746-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11746-109">설명</span><span class="sxs-lookup"><span data-stu-id="11746-109">DESCRIPTION</span></span>
<span data-ttu-id="11746-110">**Remove-AzNetAppFilesBackupPolicy** cmdlet은 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="11746-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="11746-111">예제</span><span class="sxs-lookup"><span data-stu-id="11746-111">EXAMPLES</span></span>

### <span data-ttu-id="11746-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="11746-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="11746-113">이 명령은 "MyAccount" 계정에 대해 이름이 "MyBackupPolicy"인 새 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="11746-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="11746-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11746-114">PARAMETERS</span></span>

### <span data-ttu-id="11746-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11746-115">-AccountName</span></span>
<span data-ttu-id="11746-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="11746-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="11746-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="11746-117">-AccountObject</span></span>
<span data-ttu-id="11746-118">제거할 Backup 정책이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="11746-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="11746-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11746-119">-DefaultProfile</span></span>
<span data-ttu-id="11746-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11746-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11746-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11746-121">-InputObject</span></span>
<span data-ttu-id="11746-122">제거할 BackupPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="11746-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11746-123">-Name</span><span class="sxs-lookup"><span data-stu-id="11746-123">-Name</span></span>
<span data-ttu-id="11746-124">ANF 백업 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="11746-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11746-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11746-125">-PassThru</span></span>
<span data-ttu-id="11746-126">지정된 백업 정책이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="11746-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="11746-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11746-127">-ResourceGroupName</span></span>
<span data-ttu-id="11746-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="11746-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="11746-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11746-129">-ResourceId</span></span>
<span data-ttu-id="11746-130">ANF Backup 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="11746-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="11746-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11746-131">-Confirm</span></span>
<span data-ttu-id="11746-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11746-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11746-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11746-133">-WhatIf</span></span>
<span data-ttu-id="11746-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="11746-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11746-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11746-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11746-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11746-136">CommonParameters</span></span>
<span data-ttu-id="11746-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11746-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11746-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11746-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11746-139">입력</span><span class="sxs-lookup"><span data-stu-id="11746-139">INPUTS</span></span>

### <span data-ttu-id="11746-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="11746-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="11746-141">System.String</span><span class="sxs-lookup"><span data-stu-id="11746-141">System.String</span></span>

### <span data-ttu-id="11746-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="11746-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="11746-143">출력</span><span class="sxs-lookup"><span data-stu-id="11746-143">OUTPUTS</span></span>

### <span data-ttu-id="11746-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="11746-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="11746-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11746-145">NOTES</span></span>

## <span data-ttu-id="11746-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11746-146">RELATED LINKS</span></span>
