---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: 95b7ad2ea93f1e1b22eafe3fbaae811dc33f24d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968128"
---
# <span data-ttu-id="a81a3-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="a81a3-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="a81a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a81a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a81a3-103">제공된 선택적 수정자에 대한 ANF(Azure NetApp Files) 백업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="a81a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="a81a3-104">SYNTAX</span></span>

### <span data-ttu-id="a81a3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a81a3-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a81a3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81a3-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a81a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81a3-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a81a3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a81a3-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a81a3-109">설명</span><span class="sxs-lookup"><span data-stu-id="a81a3-109">DESCRIPTION</span></span>
<span data-ttu-id="a81a3-110">**Update-AzNetAppFilesBackup** cmdlet은 ANF 백업을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="a81a3-111">예제</span><span class="sxs-lookup"><span data-stu-id="a81a3-111">EXAMPLES</span></span>

### <span data-ttu-id="a81a3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a81a3-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="a81a3-113">이 명령은 제공된 사용자 이름을 수정하는 주어진 백업에서 업데이트를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="a81a3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a81a3-114">PARAMETERS</span></span>

### <span data-ttu-id="a81a3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a81a3-115">-AccountName</span></span>
<span data-ttu-id="a81a3-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="a81a3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a81a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81a3-117">-DefaultProfile</span></span>
<span data-ttu-id="a81a3-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a81a3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a81a3-119">-InputObject</span></span>
<span data-ttu-id="a81a3-120">제거할 스냅숏 개체</span><span class="sxs-lookup"><span data-stu-id="a81a3-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a81a3-121">-Label</span><span class="sxs-lookup"><span data-stu-id="a81a3-121">-Label</span></span>
<span data-ttu-id="a81a3-122">백업용 레이블</span><span class="sxs-lookup"><span data-stu-id="a81a3-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81a3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a81a3-123">-Location</span></span>
<span data-ttu-id="a81a3-124">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="a81a3-124">The location of the resource</span></span>

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

### <span data-ttu-id="a81a3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a81a3-125">-Name</span></span>
<span data-ttu-id="a81a3-126">ANF 백업 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="a81a3-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="a81a3-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a81a3-127">-PoolName</span></span>
<span data-ttu-id="a81a3-128">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="a81a3-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a81a3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a81a3-129">-ResourceGroupName</span></span>
<span data-ttu-id="a81a3-130">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="a81a3-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a81a3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a81a3-131">-ResourceId</span></span>
<span data-ttu-id="a81a3-132">ANF Backup의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a81a3-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="a81a3-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="a81a3-133">-Tag</span></span>
<span data-ttu-id="a81a3-134">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="a81a3-134">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81a3-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="a81a3-135">-VolumeName</span></span>
<span data-ttu-id="a81a3-136">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="a81a3-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a81a3-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="a81a3-137">-VolumeObject</span></span>
<span data-ttu-id="a81a3-138">반환할 백업이 포함된 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="a81a3-138">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a81a3-139">-확인</span><span class="sxs-lookup"><span data-stu-id="a81a3-139">-Confirm</span></span>
<span data-ttu-id="a81a3-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a81a3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a81a3-141">-WhatIf</span></span>
<span data-ttu-id="a81a3-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a81a3-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a81a3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81a3-144">CommonParameters</span></span>
<span data-ttu-id="a81a3-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a81a3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81a3-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a81a3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81a3-147">입력</span><span class="sxs-lookup"><span data-stu-id="a81a3-147">INPUTS</span></span>

### <span data-ttu-id="a81a3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a81a3-148">System.String</span></span>

### <span data-ttu-id="a81a3-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a81a3-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="a81a3-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="a81a3-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="a81a3-151">출력</span><span class="sxs-lookup"><span data-stu-id="a81a3-151">OUTPUTS</span></span>

### <span data-ttu-id="a81a3-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a81a3-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="a81a3-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a81a3-153">NOTES</span></span>

## <span data-ttu-id="a81a3-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a81a3-154">RELATED LINKS</span></span>
