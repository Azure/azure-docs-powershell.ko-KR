---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: f2f930a3223b8955c7165cadab04d1fe82b2bc3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968336"
---
# <span data-ttu-id="9d51f-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="9d51f-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="9d51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d51f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d51f-103">ANF(Azure NetApp Files) 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="9d51f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d51f-104">SYNTAX</span></span>

### <span data-ttu-id="9d51f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9d51f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51f-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51f-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d51f-109">설명</span><span class="sxs-lookup"><span data-stu-id="9d51f-109">DESCRIPTION</span></span>
<span data-ttu-id="9d51f-110">**Remove-AzNetAppFilesBackup** cmdlet은 ANF 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="9d51f-111">예제</span><span class="sxs-lookup"><span data-stu-id="9d51f-111">EXAMPLES</span></span>

### <span data-ttu-id="9d51f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9d51f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="9d51f-113">이 명령은 볼륨 "MyVolume"에 대해 "MyBackup"의 이름으로 새 ANF 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="9d51f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9d51f-114">PARAMETERS</span></span>

### <span data-ttu-id="9d51f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d51f-115">-AccountName</span></span>
<span data-ttu-id="9d51f-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="9d51f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9d51f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d51f-117">-DefaultProfile</span></span>
<span data-ttu-id="9d51f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d51f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d51f-119">-InputObject</span></span>
<span data-ttu-id="9d51f-120">제거할 스냅숏 개체</span><span class="sxs-lookup"><span data-stu-id="9d51f-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="9d51f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9d51f-121">-Name</span></span>
<span data-ttu-id="9d51f-122">ANF 백업의 이름</span><span class="sxs-lookup"><span data-stu-id="9d51f-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="9d51f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d51f-123">-PassThru</span></span>
<span data-ttu-id="9d51f-124">지정된 백업이 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="9d51f-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9d51f-125">-PoolName</span></span>
<span data-ttu-id="9d51f-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="9d51f-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9d51f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d51f-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d51f-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9d51f-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9d51f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d51f-129">-ResourceId</span></span>
<span data-ttu-id="9d51f-130">ANF Backup의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9d51f-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="9d51f-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="9d51f-131">-VolumeName</span></span>
<span data-ttu-id="9d51f-132">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="9d51f-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9d51f-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="9d51f-133">-VolumeObject</span></span>
<span data-ttu-id="9d51f-134">반환할 백업이 포함된 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="9d51f-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="9d51f-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9d51f-135">-Confirm</span></span>
<span data-ttu-id="9d51f-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d51f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d51f-137">-WhatIf</span></span>
<span data-ttu-id="9d51f-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d51f-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d51f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d51f-140">CommonParameters</span></span>
<span data-ttu-id="9d51f-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d51f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d51f-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d51f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d51f-143">입력</span><span class="sxs-lookup"><span data-stu-id="9d51f-143">INPUTS</span></span>

### <span data-ttu-id="9d51f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9d51f-144">System.String</span></span>

### <span data-ttu-id="9d51f-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9d51f-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="9d51f-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="9d51f-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="9d51f-147">출력</span><span class="sxs-lookup"><span data-stu-id="9d51f-147">OUTPUTS</span></span>

### <span data-ttu-id="9d51f-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9d51f-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9d51f-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d51f-149">NOTES</span></span>

## <span data-ttu-id="9d51f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d51f-150">RELATED LINKS</span></span>
