---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47383ee57d527f6348781e57ed965e1ed8d36ef2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877291"
---
# <span data-ttu-id="14db9-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="14db9-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="14db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14db9-102">SYNOPSIS</span></span>
<span data-ttu-id="14db9-103">새 Azure NetApp Files (ANF) 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="14db9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14db9-104">SYNTAX</span></span>

### <span data-ttu-id="14db9-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="14db9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14db9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14db9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14db9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="14db9-107">DESCRIPTION</span></span>
<span data-ttu-id="14db9-108">**새 AzNetAppFilesSnapshot** cmdlet은 anf 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="14db9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="14db9-109">EXAMPLES</span></span>

### <span data-ttu-id="14db9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="14db9-110">Example 1</span></span>
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
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="14db9-111">이 명령은 "MyAnfVolume" 볼륨 내에 새 ANF 스냅샷 "MyAnfSnapshot"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="14db9-112">변수</span><span class="sxs-lookup"><span data-stu-id="14db9-112">PARAMETERS</span></span>

### <span data-ttu-id="14db9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="14db9-113">-AccountName</span></span>
<span data-ttu-id="14db9-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="14db9-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="14db9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14db9-115">-DefaultProfile</span></span>
<span data-ttu-id="14db9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14db9-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="14db9-117">-FileSystemId</span></span>
<span data-ttu-id="14db9-118">파일 시스템 id</span><span class="sxs-lookup"><span data-stu-id="14db9-118">The file system id</span></span>

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

### <span data-ttu-id="14db9-119">-위치</span><span class="sxs-lookup"><span data-stu-id="14db9-119">-Location</span></span>
<span data-ttu-id="14db9-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="14db9-120">The location of the resource</span></span>

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

### <span data-ttu-id="14db9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="14db9-121">-Name</span></span>
<span data-ttu-id="14db9-122">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="14db9-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="14db9-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="14db9-123">-PoolName</span></span>
<span data-ttu-id="14db9-124">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="14db9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14db9-125">-ResourceGroupName</span></span>
<span data-ttu-id="14db9-126">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="14db9-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="14db9-127">태그</span><span class="sxs-lookup"><span data-stu-id="14db9-127">-Tag</span></span>
<span data-ttu-id="14db9-128">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="14db9-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="14db9-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="14db9-129">-VolumeName</span></span>
<span data-ttu-id="14db9-130">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="14db9-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="14db9-131">-VolumeObject</span></span>
<span data-ttu-id="14db9-132">새 스냅숏 개체의 볼륨입니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="14db9-133">-확인</span><span class="sxs-lookup"><span data-stu-id="14db9-133">-Confirm</span></span>
<span data-ttu-id="14db9-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14db9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14db9-135">-WhatIf</span></span>
<span data-ttu-id="14db9-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14db9-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14db9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14db9-138">CommonParameters</span></span>
<span data-ttu-id="14db9-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14db9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14db9-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14db9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14db9-141">입력</span><span class="sxs-lookup"><span data-stu-id="14db9-141">INPUTS</span></span>

### <span data-ttu-id="14db9-142">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="14db9-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="14db9-143">출력</span><span class="sxs-lookup"><span data-stu-id="14db9-143">OUTPUTS</span></span>

### <span data-ttu-id="14db9-144">PSNetAppFilesSnapshot-. p m.</span><span class="sxs-lookup"><span data-stu-id="14db9-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="14db9-145">상속자</span><span class="sxs-lookup"><span data-stu-id="14db9-145">NOTES</span></span>

## <span data-ttu-id="14db9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14db9-146">RELATED LINKS</span></span>
