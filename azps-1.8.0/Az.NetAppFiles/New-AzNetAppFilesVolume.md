---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700770"
---
# <span data-ttu-id="d588d-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d588d-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d588d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d588d-102">SYNOPSIS</span></span>
<span data-ttu-id="d588d-103">새 Azure NetApp Files (ANF) 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="d588d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d588d-104">SYNTAX</span></span>

### <span data-ttu-id="d588d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d588d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d588d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d588d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d588d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d588d-107">DESCRIPTION</span></span>
<span data-ttu-id="d588d-108">**새 AzNetAppFilesVolume** cmdlet은 anf 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="d588d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d588d-109">EXAMPLES</span></span>

### <span data-ttu-id="d588d-110">예제 1: ANF 볼륨 만들기</span><span class="sxs-lookup"><span data-stu-id="d588d-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="d588d-111">이 명령은 "MyAnfPool" 풀 내에 새 ANF 볼륨 "MyAnfVolume"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="d588d-112">변수</span><span class="sxs-lookup"><span data-stu-id="d588d-112">PARAMETERS</span></span>

### <span data-ttu-id="d588d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d588d-113">-AccountName</span></span>
<span data-ttu-id="d588d-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="d588d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="d588d-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="d588d-115">-CreationToken</span></span>
<span data-ttu-id="d588d-116">볼륨에 대 한 고유한 파일 경로</span><span class="sxs-lookup"><span data-stu-id="d588d-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d588d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d588d-117">-DefaultProfile</span></span>
<span data-ttu-id="d588d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d588d-119">-위치</span><span class="sxs-lookup"><span data-stu-id="d588d-119">-Location</span></span>
<span data-ttu-id="d588d-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="d588d-120">The location of the resource</span></span>

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

### <span data-ttu-id="d588d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d588d-121">-Name</span></span>
<span data-ttu-id="d588d-122">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d588d-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d588d-123">-PoolName</span></span>
<span data-ttu-id="d588d-124">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d588d-125">-Poo</span><span class="sxs-lookup"><span data-stu-id="d588d-125">-PoolObject</span></span>
<span data-ttu-id="d588d-126">새 볼륨 개체에 대 한 풀</span><span class="sxs-lookup"><span data-stu-id="d588d-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="d588d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d588d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d588d-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="d588d-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d588d-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d588d-129">-ServiceLevel</span></span>
<span data-ttu-id="d588d-130">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="d588d-130">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d588d-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d588d-131">-SubnetId</span></span>
<span data-ttu-id="d588d-132">위임 된 서브넷에 대 한 Azure 리소스 URI</span><span class="sxs-lookup"><span data-stu-id="d588d-132">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d588d-133">태그</span><span class="sxs-lookup"><span data-stu-id="d588d-133">-Tag</span></span>
<span data-ttu-id="d588d-134">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="d588d-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d588d-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d588d-135">-UsageThreshold</span></span>
<span data-ttu-id="d588d-136">파일 시스템에 허용 되는 최대 저장소 할당량 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-136">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d588d-137">-확인</span><span class="sxs-lookup"><span data-stu-id="d588d-137">-Confirm</span></span>
<span data-ttu-id="d588d-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d588d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d588d-139">-WhatIf</span></span>
<span data-ttu-id="d588d-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d588d-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d588d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d588d-142">CommonParameters</span></span>
<span data-ttu-id="d588d-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d588d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d588d-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d588d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d588d-145">입력</span><span class="sxs-lookup"><span data-stu-id="d588d-145">INPUTS</span></span>

### <span data-ttu-id="d588d-146">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d588d-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="d588d-147">출력</span><span class="sxs-lookup"><span data-stu-id="d588d-147">OUTPUTS</span></span>

### <span data-ttu-id="d588d-148">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d588d-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d588d-149">상속자</span><span class="sxs-lookup"><span data-stu-id="d588d-149">NOTES</span></span>

## <span data-ttu-id="d588d-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d588d-150">RELATED LINKS</span></span>
