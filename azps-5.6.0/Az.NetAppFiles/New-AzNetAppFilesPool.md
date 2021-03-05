---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: 30a569c16a2f3da135f77061e8ff5373c45b2598
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968448"
---
# <span data-ttu-id="34300-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="34300-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="34300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34300-102">SYNOPSIS</span></span>
<span data-ttu-id="34300-103">ANF(새 Azure NetApp Files) 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34300-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="34300-104">구문</span><span class="sxs-lookup"><span data-stu-id="34300-104">SYNTAX</span></span>

### <span data-ttu-id="34300-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="34300-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34300-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34300-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34300-107">설명</span><span class="sxs-lookup"><span data-stu-id="34300-107">DESCRIPTION</span></span>
<span data-ttu-id="34300-108">**New-AzNetAppFilesPool** cmdlet은 ANF 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34300-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="34300-109">예제</span><span class="sxs-lookup"><span data-stu-id="34300-109">EXAMPLES</span></span>

### <span data-ttu-id="34300-110">예제 1: ANF 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="34300-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="34300-111">이 명령은 "MyAnfAccount"의 계정 내에 새 ANF 풀 "MyAnfPool"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34300-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="34300-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="34300-112">PARAMETERS</span></span>

### <span data-ttu-id="34300-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34300-113">-AccountName</span></span>
<span data-ttu-id="34300-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="34300-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="34300-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="34300-115">-AccountObject</span></span>
<span data-ttu-id="34300-116">새 풀 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="34300-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="34300-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34300-117">-DefaultProfile</span></span>
<span data-ttu-id="34300-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34300-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34300-119">-Location</span><span class="sxs-lookup"><span data-stu-id="34300-119">-Location</span></span>
<span data-ttu-id="34300-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="34300-120">The location of the resource</span></span>

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

### <span data-ttu-id="34300-121">-Name</span><span class="sxs-lookup"><span data-stu-id="34300-121">-Name</span></span>
<span data-ttu-id="34300-122">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="34300-122">The name of the ANF pool</span></span>

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

### <span data-ttu-id="34300-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="34300-123">-PoolSize</span></span>
<span data-ttu-id="34300-124">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="34300-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="34300-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="34300-125">-QosType</span></span>
<span data-ttu-id="34300-126">풀의 qos 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="34300-126">The qos type of the pool.</span></span> <span data-ttu-id="34300-127">가능한 값은 다음과 같습니다. '자동', '수동'</span><span class="sxs-lookup"><span data-stu-id="34300-127">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="34300-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34300-128">-ResourceGroupName</span></span>
<span data-ttu-id="34300-129">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="34300-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="34300-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="34300-130">-ServiceLevel</span></span>
<span data-ttu-id="34300-131">ANF 풀의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="34300-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="34300-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="34300-132">-Tag</span></span>
<span data-ttu-id="34300-133">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="34300-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="34300-134">-확인</span><span class="sxs-lookup"><span data-stu-id="34300-134">-Confirm</span></span>
<span data-ttu-id="34300-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34300-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34300-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34300-136">-WhatIf</span></span>
<span data-ttu-id="34300-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="34300-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34300-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34300-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34300-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34300-139">CommonParameters</span></span>
<span data-ttu-id="34300-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34300-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34300-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34300-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34300-142">입력</span><span class="sxs-lookup"><span data-stu-id="34300-142">INPUTS</span></span>

### <span data-ttu-id="34300-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="34300-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="34300-144">출력</span><span class="sxs-lookup"><span data-stu-id="34300-144">OUTPUTS</span></span>

### <span data-ttu-id="34300-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="34300-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="34300-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34300-146">NOTES</span></span>

## <span data-ttu-id="34300-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34300-147">RELATED LINKS</span></span>
