---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489980"
---
# <span data-ttu-id="ea965-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ea965-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="ea965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea965-102">SYNOPSIS</span></span>
<span data-ttu-id="ea965-103">새 ANF(Azure NetApp Files) 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="ea965-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea965-104">SYNTAX</span></span>

### <span data-ttu-id="ea965-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ea965-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea965-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea965-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea965-107">설명</span><span class="sxs-lookup"><span data-stu-id="ea965-107">DESCRIPTION</span></span>
<span data-ttu-id="ea965-108">**New-AzNetAppFilesPool** cmdlet은 ANF 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="ea965-109">예제</span><span class="sxs-lookup"><span data-stu-id="ea965-109">EXAMPLES</span></span>

### <span data-ttu-id="ea965-110">예제 1: ANF 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="ea965-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="ea965-111">이 명령은 "MyAnfAccount" 계정 내에 새 ANF 풀 "MyAnfPool"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="ea965-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea965-112">PARAMETERS</span></span>

### <span data-ttu-id="ea965-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea965-113">-AccountName</span></span>
<span data-ttu-id="ea965-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="ea965-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="ea965-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ea965-115">-AccountObject</span></span>
<span data-ttu-id="ea965-116">새 풀 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="ea965-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="ea965-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea965-117">-DefaultProfile</span></span>
<span data-ttu-id="ea965-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea965-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ea965-119">-Location</span></span>
<span data-ttu-id="ea965-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="ea965-120">The location of the resource</span></span>

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

### <span data-ttu-id="ea965-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ea965-121">-Name</span></span>
<span data-ttu-id="ea965-122">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="ea965-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea965-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="ea965-123">-PoolSize</span></span>
<span data-ttu-id="ea965-124">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="ea965-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea965-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="ea965-125">-QosType</span></span>
<span data-ttu-id="ea965-126">풀의 qos 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-126">The qos type of the pool.</span></span> <span data-ttu-id="ea965-127">가능한 값은 'Auto', 'Manual'입니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea965-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea965-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea965-129">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ea965-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ea965-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="ea965-130">-ServiceLevel</span></span>
<span data-ttu-id="ea965-131">ANF 풀의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="ea965-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="ea965-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea965-132">-Tag</span></span>
<span data-ttu-id="ea965-133">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="ea965-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ea965-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea965-134">-Confirm</span></span>
<span data-ttu-id="ea965-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea965-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea965-136">-WhatIf</span></span>
<span data-ttu-id="ea965-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ea965-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea965-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea965-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea965-139">CommonParameters</span></span>
<span data-ttu-id="ea965-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea965-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea965-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea965-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea965-142">입력</span><span class="sxs-lookup"><span data-stu-id="ea965-142">INPUTS</span></span>

### <span data-ttu-id="ea965-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ea965-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ea965-144">출력</span><span class="sxs-lookup"><span data-stu-id="ea965-144">OUTPUTS</span></span>

### <span data-ttu-id="ea965-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ea965-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="ea965-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea965-146">NOTES</span></span>

## <span data-ttu-id="ea965-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea965-147">RELATED LINKS</span></span>
