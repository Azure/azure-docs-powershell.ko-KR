---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 51d35fb3708e2b6a88daf12c2df8a0bec9990c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870937"
---
# <span data-ttu-id="e660e-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="e660e-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="e660e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e660e-102">SYNOPSIS</span></span>
<span data-ttu-id="e660e-103">새 Azure NetApp Files (ANF) 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="e660e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e660e-104">SYNTAX</span></span>

### <span data-ttu-id="e660e-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e660e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e660e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e660e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e660e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e660e-107">DESCRIPTION</span></span>
<span data-ttu-id="e660e-108">**새 AzNetAppFilesSnapshot** cmdlet은 anf 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="e660e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e660e-109">EXAMPLES</span></span>

### <span data-ttu-id="e660e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e660e-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="e660e-111">이 명령은 "MyAnfVolume" 볼륨 내에 새 ANF 스냅샷 "MyAnfSnapshot"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="e660e-112">변수</span><span class="sxs-lookup"><span data-stu-id="e660e-112">PARAMETERS</span></span>

### <span data-ttu-id="e660e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e660e-113">-AccountName</span></span>
<span data-ttu-id="e660e-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="e660e-114">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e660e-115">-DefaultProfile</span></span>
<span data-ttu-id="e660e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="e660e-117">-FileSystemId</span></span>
<span data-ttu-id="e660e-118">파일 시스템 id</span><span class="sxs-lookup"><span data-stu-id="e660e-118">The file system id</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-119">-위치</span><span class="sxs-lookup"><span data-stu-id="e660e-119">-Location</span></span>
<span data-ttu-id="e660e-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="e660e-120">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e660e-121">-Name</span></span>
<span data-ttu-id="e660e-122">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="e660e-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e660e-123">-PoolName</span></span>
<span data-ttu-id="e660e-124">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e660e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e660e-126">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="e660e-126">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-127">태그</span><span class="sxs-lookup"><span data-stu-id="e660e-127">-Tag</span></span>
<span data-ttu-id="e660e-128">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="e660e-128">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="e660e-129">-VolumeName</span></span>
<span data-ttu-id="e660e-130">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-130">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="e660e-131">-VolumeObject</span></span>
<span data-ttu-id="e660e-132">새 스냅숏 개체의 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-133">-확인</span><span class="sxs-lookup"><span data-stu-id="e660e-133">-Confirm</span></span>
<span data-ttu-id="e660e-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e660e-135">-WhatIf</span></span>
<span data-ttu-id="e660e-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e660e-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e660e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e660e-138">CommonParameters</span></span>
<span data-ttu-id="e660e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e660e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e660e-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e660e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e660e-141">입력</span><span class="sxs-lookup"><span data-stu-id="e660e-141">INPUTS</span></span>

### <span data-ttu-id="e660e-142">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e660e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e660e-143">출력</span><span class="sxs-lookup"><span data-stu-id="e660e-143">OUTPUTS</span></span>

### <span data-ttu-id="e660e-144">PSNetAppFilesSnapshot-. p m.</span><span class="sxs-lookup"><span data-stu-id="e660e-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="e660e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="e660e-145">NOTES</span></span>

## <span data-ttu-id="e660e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e660e-146">RELATED LINKS</span></span>
