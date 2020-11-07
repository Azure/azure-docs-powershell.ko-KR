---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700758"
---
# <span data-ttu-id="c3ef7-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c3ef7-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c3ef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ef7-103">제공 되는 선택적 한정자에 따라 Azure NetApp Files (ANF) 볼륨을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c3ef7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3ef7-104">SYNTAX</span></span>

### <span data-ttu-id="c3ef7-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c3ef7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3ef7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3ef7-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3ef7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3ef7-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3ef7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c3ef7-108">DESCRIPTION</span></span>
<span data-ttu-id="c3ef7-109">**업데이트 AzNetAppFilesVolume** cmdlet은 anf 볼륨을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="c3ef7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c3ef7-110">EXAMPLES</span></span>

### <span data-ttu-id="c3ef7-111">예제 1: ANF 볼륨 업데이트</span><span class="sxs-lookup"><span data-stu-id="c3ef7-111">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="c3ef7-112">이 명령은 ANF 볼륨 "MyAnfVolume"를 새로운 UsageThreshold 크기로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="c3ef7-113">변수</span><span class="sxs-lookup"><span data-stu-id="c3ef7-113">PARAMETERS</span></span>

### <span data-ttu-id="c3ef7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c3ef7-114">-AccountName</span></span>
<span data-ttu-id="c3ef7-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="c3ef7-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="c3ef7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ef7-116">-DefaultProfile</span></span>
<span data-ttu-id="c3ef7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3ef7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3ef7-118">-InputObject</span></span>
<span data-ttu-id="c3ef7-119">업데이트할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="c3ef7-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ef7-120">-위치</span><span class="sxs-lookup"><span data-stu-id="c3ef7-120">-Location</span></span>
<span data-ttu-id="c3ef7-121">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="c3ef7-121">The location of the resource</span></span>

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

### <span data-ttu-id="c3ef7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c3ef7-122">-Name</span></span>
<span data-ttu-id="c3ef7-123">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ef7-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c3ef7-124">-PoolName</span></span>
<span data-ttu-id="c3ef7-125">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-125">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c3ef7-126">-Poo</span><span class="sxs-lookup"><span data-stu-id="c3ef7-126">-PoolObject</span></span>
<span data-ttu-id="c3ef7-127">업데이트할 볼륨을 포함 하는 pool 개체</span><span class="sxs-lookup"><span data-stu-id="c3ef7-127">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ef7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ef7-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3ef7-129">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="c3ef7-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c3ef7-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c3ef7-130">-ServiceLevel</span></span>
<span data-ttu-id="c3ef7-131">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="c3ef7-131">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ef7-132">태그</span><span class="sxs-lookup"><span data-stu-id="c3ef7-132">-Tag</span></span>
<span data-ttu-id="c3ef7-133">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="c3ef7-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c3ef7-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="c3ef7-134">-UsageThreshold</span></span>
<span data-ttu-id="c3ef7-135">파일 시스템에 허용 되는 최대 저장소 할당량 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-135">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ef7-136">-확인</span><span class="sxs-lookup"><span data-stu-id="c3ef7-136">-Confirm</span></span>
<span data-ttu-id="c3ef7-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ef7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ef7-138">-WhatIf</span></span>
<span data-ttu-id="c3ef7-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ef7-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ef7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ef7-141">CommonParameters</span></span>
<span data-ttu-id="c3ef7-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ef7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c3ef7-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ef7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ef7-144">입력</span><span class="sxs-lookup"><span data-stu-id="c3ef7-144">INPUTS</span></span>

### <span data-ttu-id="c3ef7-145">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c3ef7-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="c3ef7-146">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c3ef7-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c3ef7-147">출력</span><span class="sxs-lookup"><span data-stu-id="c3ef7-147">OUTPUTS</span></span>

### <span data-ttu-id="c3ef7-148">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c3ef7-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c3ef7-149">상속자</span><span class="sxs-lookup"><span data-stu-id="c3ef7-149">NOTES</span></span>

## <span data-ttu-id="c3ef7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3ef7-150">RELATED LINKS</span></span>
