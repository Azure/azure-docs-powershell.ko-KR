---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: f7dc2473818b1e80503a4583993d818818c9aec0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870926"
---
# <span data-ttu-id="751e8-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="751e8-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="751e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="751e8-102">SYNOPSIS</span></span>
<span data-ttu-id="751e8-103">제공 되는 선택적 한정자에 따라 Azure NetApp Files (ANF) 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="751e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="751e8-104">SYNTAX</span></span>

### <span data-ttu-id="751e8-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="751e8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="751e8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="751e8-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="751e8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="751e8-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="751e8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="751e8-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="751e8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="751e8-109">DESCRIPTION</span></span>
<span data-ttu-id="751e8-110">**업데이트 AzNetAppFilesPool** cmdlet은 anf 풀을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="751e8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="751e8-111">EXAMPLES</span></span>

### <span data-ttu-id="751e8-112">예제 1: ANF 풀 수정</span><span class="sxs-lookup"><span data-stu-id="751e8-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="751e8-113">이 명령은 ANF 풀 "MyAnfPool"를 지정 된 크기와 ServiceLevel으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="751e8-114">변수</span><span class="sxs-lookup"><span data-stu-id="751e8-114">PARAMETERS</span></span>

### <span data-ttu-id="751e8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="751e8-115">-AccountName</span></span>
<span data-ttu-id="751e8-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="751e8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="751e8-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="751e8-117">-AccountObject</span></span>
<span data-ttu-id="751e8-118">업데이트할 풀을 포함 하는 account 개체</span><span class="sxs-lookup"><span data-stu-id="751e8-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="751e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751e8-119">-DefaultProfile</span></span>
<span data-ttu-id="751e8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="751e8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="751e8-121">-InputObject</span></span>
<span data-ttu-id="751e8-122">업데이트할 풀 개체</span><span class="sxs-lookup"><span data-stu-id="751e8-122">The pool object to update</span></span>

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

### <span data-ttu-id="751e8-123">-위치</span><span class="sxs-lookup"><span data-stu-id="751e8-123">-Location</span></span>
<span data-ttu-id="751e8-124">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="751e8-124">The location of the resource</span></span>

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

### <span data-ttu-id="751e8-125">-이름</span><span class="sxs-lookup"><span data-stu-id="751e8-125">-Name</span></span>
<span data-ttu-id="751e8-126">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="751e8-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="751e8-127">-PoolSize</span></span>
<span data-ttu-id="751e8-128">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="751e8-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="751e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="751e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="751e8-130">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="751e8-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="751e8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="751e8-131">-ResourceId</span></span>
<span data-ttu-id="751e8-132">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="751e8-132">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="751e8-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="751e8-133">-ServiceLevel</span></span>
<span data-ttu-id="751e8-134">ANF 풀의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="751e8-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="751e8-135">태그</span><span class="sxs-lookup"><span data-stu-id="751e8-135">-Tag</span></span>
<span data-ttu-id="751e8-136">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="751e8-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="751e8-137">-확인</span><span class="sxs-lookup"><span data-stu-id="751e8-137">-Confirm</span></span>
<span data-ttu-id="751e8-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="751e8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="751e8-139">-WhatIf</span></span>
<span data-ttu-id="751e8-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="751e8-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="751e8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751e8-142">CommonParameters</span></span>
<span data-ttu-id="751e8-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="751e8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="751e8-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="751e8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751e8-145">입력</span><span class="sxs-lookup"><span data-stu-id="751e8-145">INPUTS</span></span>

### <span data-ttu-id="751e8-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="751e8-146">System.String</span></span>

### <span data-ttu-id="751e8-147">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="751e8-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="751e8-148">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="751e8-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="751e8-149">출력</span><span class="sxs-lookup"><span data-stu-id="751e8-149">OUTPUTS</span></span>

### <span data-ttu-id="751e8-150">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="751e8-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="751e8-151">상속자</span><span class="sxs-lookup"><span data-stu-id="751e8-151">NOTES</span></span>

## <span data-ttu-id="751e8-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="751e8-152">RELATED LINKS</span></span>
