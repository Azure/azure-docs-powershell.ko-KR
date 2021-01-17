---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489987"
---
# <span data-ttu-id="3710f-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="3710f-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="3710f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3710f-102">SYNOPSIS</span></span>
<span data-ttu-id="3710f-103">새 ANF(Azure NetApp Files) 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="3710f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3710f-104">SYNTAX</span></span>

### <span data-ttu-id="3710f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3710f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3710f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3710f-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3710f-107">설명</span><span class="sxs-lookup"><span data-stu-id="3710f-107">DESCRIPTION</span></span>
<span data-ttu-id="3710f-108">**New-AzNetAppFilesBackup** cmdlet은 ANF 볼륨에 대한 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="3710f-109">예제</span><span class="sxs-lookup"><span data-stu-id="3710f-109">EXAMPLES</span></span>

### <span data-ttu-id="3710f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3710f-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="3710f-111">이 명령은 "MyVolume" 계정이라는 볼륨에 대한 새 ANF 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="3710f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3710f-112">PARAMETERS</span></span>

### <span data-ttu-id="3710f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3710f-113">-AccountName</span></span>
<span data-ttu-id="3710f-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="3710f-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="3710f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3710f-115">-DefaultProfile</span></span>
<span data-ttu-id="3710f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3710f-117">-Label</span><span class="sxs-lookup"><span data-stu-id="3710f-117">-Label</span></span>
<span data-ttu-id="3710f-118">백업 레이블</span><span class="sxs-lookup"><span data-stu-id="3710f-118">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3710f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3710f-119">-Location</span></span>
<span data-ttu-id="3710f-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="3710f-120">The location of the resource</span></span>

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

### <span data-ttu-id="3710f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3710f-121">-Name</span></span>
<span data-ttu-id="3710f-122">ANF 백업의 이름</span><span class="sxs-lookup"><span data-stu-id="3710f-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3710f-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3710f-123">-PoolName</span></span>
<span data-ttu-id="3710f-124">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="3710f-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3710f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3710f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3710f-126">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="3710f-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3710f-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="3710f-127">-VolumeName</span></span>
<span data-ttu-id="3710f-128">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="3710f-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="3710f-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="3710f-129">-VolumeObject</span></span>
<span data-ttu-id="3710f-130">새 백업 개체의 볼륨</span><span class="sxs-lookup"><span data-stu-id="3710f-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="3710f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3710f-131">-Confirm</span></span>
<span data-ttu-id="3710f-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3710f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3710f-133">-WhatIf</span></span>
<span data-ttu-id="3710f-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3710f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3710f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3710f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3710f-136">CommonParameters</span></span>
<span data-ttu-id="3710f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3710f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3710f-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3710f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3710f-139">입력</span><span class="sxs-lookup"><span data-stu-id="3710f-139">INPUTS</span></span>

### <span data-ttu-id="3710f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3710f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3710f-141">출력</span><span class="sxs-lookup"><span data-stu-id="3710f-141">OUTPUTS</span></span>

### <span data-ttu-id="3710f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="3710f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="3710f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3710f-143">NOTES</span></span>

## <span data-ttu-id="3710f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3710f-144">RELATED LINKS</span></span>
