---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700759"
---
# <span data-ttu-id="59ec6-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="59ec6-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="59ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="59ec6-103">새 데이터 집합으로 Azure NetApp Files (ANF) 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="59ec6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59ec6-104">SYNTAX</span></span>

### <span data-ttu-id="59ec6-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="59ec6-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59ec6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59ec6-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59ec6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59ec6-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59ec6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="59ec6-108">DESCRIPTION</span></span>
<span data-ttu-id="59ec6-109">**업데이트 AzNetAppFilesPool** cmdlet은 anf 풀을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="59ec6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="59ec6-110">EXAMPLES</span></span>

### <span data-ttu-id="59ec6-111">예제 1: ANF 풀 수정</span><span class="sxs-lookup"><span data-stu-id="59ec6-111">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="59ec6-112">이 명령은 ANF 풀 "MyAnfPool"를 지정 된 크기와 ServiceLevel으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="59ec6-113">변수</span><span class="sxs-lookup"><span data-stu-id="59ec6-113">PARAMETERS</span></span>

### <span data-ttu-id="59ec6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59ec6-114">-AccountName</span></span>
<span data-ttu-id="59ec6-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="59ec6-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="59ec6-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="59ec6-116">-AccountObject</span></span>
<span data-ttu-id="59ec6-117">업데이트할 풀을 포함 하는 account 개체</span><span class="sxs-lookup"><span data-stu-id="59ec6-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ec6-118">-DefaultProfile</span></span>
<span data-ttu-id="59ec6-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59ec6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59ec6-120">-InputObject</span></span>
<span data-ttu-id="59ec6-121">업데이트할 풀 개체</span><span class="sxs-lookup"><span data-stu-id="59ec6-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-122">-위치</span><span class="sxs-lookup"><span data-stu-id="59ec6-122">-Location</span></span>
<span data-ttu-id="59ec6-123">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="59ec6-123">The location of the resource</span></span>

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

### <span data-ttu-id="59ec6-124">-이름</span><span class="sxs-lookup"><span data-stu-id="59ec6-124">-Name</span></span>
<span data-ttu-id="59ec6-125">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="59ec6-126">-PoolSize</span></span>
<span data-ttu-id="59ec6-127">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="59ec6-127">The size of the ANF pool</span></span>

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

### <span data-ttu-id="59ec6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ec6-128">-ResourceGroupName</span></span>
<span data-ttu-id="59ec6-129">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="59ec6-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="59ec6-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="59ec6-130">-ServiceLevel</span></span>
<span data-ttu-id="59ec6-131">ANF 풀의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="59ec6-131">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="59ec6-132">-확인</span><span class="sxs-lookup"><span data-stu-id="59ec6-132">-Confirm</span></span>
<span data-ttu-id="59ec6-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59ec6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59ec6-134">-WhatIf</span></span>
<span data-ttu-id="59ec6-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59ec6-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59ec6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ec6-137">CommonParameters</span></span>
<span data-ttu-id="59ec6-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ec6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="59ec6-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ec6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ec6-140">입력</span><span class="sxs-lookup"><span data-stu-id="59ec6-140">INPUTS</span></span>

### <span data-ttu-id="59ec6-141">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="59ec6-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="59ec6-142">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="59ec6-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="59ec6-143">출력</span><span class="sxs-lookup"><span data-stu-id="59ec6-143">OUTPUTS</span></span>

### <span data-ttu-id="59ec6-144">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="59ec6-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="59ec6-145">상속자</span><span class="sxs-lookup"><span data-stu-id="59ec6-145">NOTES</span></span>

## <span data-ttu-id="59ec6-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59ec6-146">RELATED LINKS</span></span>
