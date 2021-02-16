---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192052"
---
# <span data-ttu-id="eb836-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="eb836-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="eb836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb836-102">SYNOPSIS</span></span>
<span data-ttu-id="eb836-103">ANF(Azure NetApp Files) 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="eb836-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb836-104">SYNTAX</span></span>

### <span data-ttu-id="eb836-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eb836-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb836-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb836-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb836-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb836-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb836-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb836-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb836-109">설명</span><span class="sxs-lookup"><span data-stu-id="eb836-109">DESCRIPTION</span></span>
<span data-ttu-id="eb836-110">**Remove-AzNetAppFilesBackup** cmdlet은 ANF 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="eb836-111">예제</span><span class="sxs-lookup"><span data-stu-id="eb836-111">EXAMPLES</span></span>

### <span data-ttu-id="eb836-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="eb836-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="eb836-113">이 명령은 볼륨 "MyVolume"에 대해 이름이 "MyBackup"인 새 ANF 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="eb836-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb836-114">PARAMETERS</span></span>

### <span data-ttu-id="eb836-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb836-115">-AccountName</span></span>
<span data-ttu-id="eb836-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="eb836-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb836-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb836-117">-DefaultProfile</span></span>
<span data-ttu-id="eb836-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb836-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb836-119">-InputObject</span></span>
<span data-ttu-id="eb836-120">제거할 스냅숏 개체</span><span class="sxs-lookup"><span data-stu-id="eb836-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="eb836-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb836-121">-Name</span></span>
<span data-ttu-id="eb836-122">ANF 백업의 이름</span><span class="sxs-lookup"><span data-stu-id="eb836-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb836-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb836-123">-PassThru</span></span>
<span data-ttu-id="eb836-124">지정된 백업이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="eb836-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="eb836-125">-PoolName</span></span>
<span data-ttu-id="eb836-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="eb836-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="eb836-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb836-127">-ResourceGroupName</span></span>
<span data-ttu-id="eb836-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="eb836-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="eb836-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb836-129">-ResourceId</span></span>
<span data-ttu-id="eb836-130">ANF Backup의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="eb836-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="eb836-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="eb836-131">-VolumeName</span></span>
<span data-ttu-id="eb836-132">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="eb836-132">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb836-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="eb836-133">-VolumeObject</span></span>
<span data-ttu-id="eb836-134">반환할 백업이 포함된 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="eb836-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="eb836-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb836-135">-Confirm</span></span>
<span data-ttu-id="eb836-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb836-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb836-137">-WhatIf</span></span>
<span data-ttu-id="eb836-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eb836-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb836-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb836-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb836-140">CommonParameters</span></span>
<span data-ttu-id="eb836-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb836-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb836-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb836-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb836-143">입력</span><span class="sxs-lookup"><span data-stu-id="eb836-143">INPUTS</span></span>

### <span data-ttu-id="eb836-144">System.String</span><span class="sxs-lookup"><span data-stu-id="eb836-144">System.String</span></span>

### <span data-ttu-id="eb836-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eb836-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="eb836-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="eb836-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="eb836-147">출력</span><span class="sxs-lookup"><span data-stu-id="eb836-147">OUTPUTS</span></span>

### <span data-ttu-id="eb836-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="eb836-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="eb836-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb836-149">NOTES</span></span>

## <span data-ttu-id="eb836-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb836-150">RELATED LINKS</span></span>
