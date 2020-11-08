---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047727"
---
# <span data-ttu-id="aec72-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="aec72-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="aec72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec72-102">SYNOPSIS</span></span>
<span data-ttu-id="aec72-103">제공 되는 선택적 한정자에 따라 Azure NetApp Files (ANF) 볼륨을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="aec72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aec72-104">SYNTAX</span></span>

### <span data-ttu-id="aec72-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aec72-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec72-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aec72-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec72-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aec72-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec72-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aec72-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec72-109">설명은</span><span class="sxs-lookup"><span data-stu-id="aec72-109">DESCRIPTION</span></span>
<span data-ttu-id="aec72-110">**업데이트 AzNetAppFilesVolume** cmdlet은 anf 볼륨을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="aec72-111">예제의</span><span class="sxs-lookup"><span data-stu-id="aec72-111">EXAMPLES</span></span>

### <span data-ttu-id="aec72-112">예제 1: ANF 볼륨 업데이트</span><span class="sxs-lookup"><span data-stu-id="aec72-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="aec72-113">이 명령은 ANF 볼륨 "MyAnfVolume"를 새로운 UsageThreshold 크기로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="aec72-114">변수</span><span class="sxs-lookup"><span data-stu-id="aec72-114">PARAMETERS</span></span>

### <span data-ttu-id="aec72-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aec72-115">-AccountName</span></span>
<span data-ttu-id="aec72-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="aec72-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="aec72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec72-117">-DefaultProfile</span></span>
<span data-ttu-id="aec72-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec72-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="aec72-119">-ExportPolicy</span></span>
<span data-ttu-id="aec72-120">내보내기 정책을 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="aec72-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec72-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aec72-121">-InputObject</span></span>
<span data-ttu-id="aec72-122">업데이트할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="aec72-122">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aec72-123">-위치</span><span class="sxs-lookup"><span data-stu-id="aec72-123">-Location</span></span>
<span data-ttu-id="aec72-124">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="aec72-124">The location of the resource</span></span>

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

### <span data-ttu-id="aec72-125">-이름</span><span class="sxs-lookup"><span data-stu-id="aec72-125">-Name</span></span>
<span data-ttu-id="aec72-126">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-126">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec72-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="aec72-127">-PoolName</span></span>
<span data-ttu-id="aec72-128">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="aec72-129">-Poo</span><span class="sxs-lookup"><span data-stu-id="aec72-129">-PoolObject</span></span>
<span data-ttu-id="aec72-130">업데이트할 볼륨을 포함 하는 pool 개체</span><span class="sxs-lookup"><span data-stu-id="aec72-130">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aec72-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec72-131">-ResourceGroupName</span></span>
<span data-ttu-id="aec72-132">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="aec72-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="aec72-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aec72-133">-ResourceId</span></span>
<span data-ttu-id="aec72-134">ANF 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="aec72-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="aec72-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="aec72-135">-ServiceLevel</span></span>
<span data-ttu-id="aec72-136">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="aec72-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="aec72-137">태그</span><span class="sxs-lookup"><span data-stu-id="aec72-137">-Tag</span></span>
<span data-ttu-id="aec72-138">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="aec72-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="aec72-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="aec72-139">-UsageThreshold</span></span>
<span data-ttu-id="aec72-140">파일 시스템에 허용 되는 최대 저장소 할당량 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec72-141">-확인</span><span class="sxs-lookup"><span data-stu-id="aec72-141">-Confirm</span></span>
<span data-ttu-id="aec72-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec72-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec72-143">-WhatIf</span></span>
<span data-ttu-id="aec72-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec72-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec72-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec72-146">CommonParameters</span></span>
<span data-ttu-id="aec72-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec72-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec72-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aec72-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec72-149">입력</span><span class="sxs-lookup"><span data-stu-id="aec72-149">INPUTS</span></span>

### <span data-ttu-id="aec72-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aec72-150">System.String</span></span>

### <span data-ttu-id="aec72-151">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="aec72-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="aec72-152">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="aec72-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="aec72-153">출력</span><span class="sxs-lookup"><span data-stu-id="aec72-153">OUTPUTS</span></span>

### <span data-ttu-id="aec72-154">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="aec72-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="aec72-155">상속자</span><span class="sxs-lookup"><span data-stu-id="aec72-155">NOTES</span></span>

## <span data-ttu-id="aec72-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aec72-156">RELATED LINKS</span></span>
