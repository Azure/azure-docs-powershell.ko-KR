---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: bea1f6d9427d0ed5dca48994d8138f954ed25ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877271"
---
# <span data-ttu-id="3bfce-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3bfce-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="3bfce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bfce-102">SYNOPSIS</span></span>
<span data-ttu-id="3bfce-103">제공 되는 선택적 한정자에 따라 Azure NetApp Files (ANF) 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="3bfce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bfce-104">SYNTAX</span></span>

### <span data-ttu-id="3bfce-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3bfce-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bfce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bfce-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bfce-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bfce-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bfce-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bfce-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bfce-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3bfce-109">DESCRIPTION</span></span>
<span data-ttu-id="3bfce-110">**업데이트 AzNetAppFilesPool** cmdlet은 anf 풀을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="3bfce-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3bfce-111">EXAMPLES</span></span>

### <span data-ttu-id="3bfce-112">예제 1: ANF 풀 수정</span><span class="sxs-lookup"><span data-stu-id="3bfce-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="3bfce-113">이 명령은 ANF 풀 "MyAnfPool"를 지정 된 크기와 ServiceLevel으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="3bfce-114">변수</span><span class="sxs-lookup"><span data-stu-id="3bfce-114">PARAMETERS</span></span>

### <span data-ttu-id="3bfce-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3bfce-115">-AccountName</span></span>
<span data-ttu-id="3bfce-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="3bfce-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="3bfce-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="3bfce-117">-AccountObject</span></span>
<span data-ttu-id="3bfce-118">업데이트할 풀을 포함 하는 account 개체</span><span class="sxs-lookup"><span data-stu-id="3bfce-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="3bfce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bfce-119">-DefaultProfile</span></span>
<span data-ttu-id="3bfce-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bfce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bfce-121">-InputObject</span></span>
<span data-ttu-id="3bfce-122">업데이트할 풀 개체</span><span class="sxs-lookup"><span data-stu-id="3bfce-122">The pool object to update</span></span>

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

### <span data-ttu-id="3bfce-123">-위치</span><span class="sxs-lookup"><span data-stu-id="3bfce-123">-Location</span></span>
<span data-ttu-id="3bfce-124">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="3bfce-124">The location of the resource</span></span>

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

### <span data-ttu-id="3bfce-125">-이름</span><span class="sxs-lookup"><span data-stu-id="3bfce-125">-Name</span></span>
<span data-ttu-id="3bfce-126">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3bfce-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="3bfce-127">-PoolSize</span></span>
<span data-ttu-id="3bfce-128">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="3bfce-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="3bfce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bfce-129">-ResourceGroupName</span></span>
<span data-ttu-id="3bfce-130">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="3bfce-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3bfce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bfce-131">-ResourceId</span></span>
<span data-ttu-id="3bfce-132">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="3bfce-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="3bfce-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="3bfce-133">-ServiceLevel</span></span>
<span data-ttu-id="3bfce-134">ANF 풀의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="3bfce-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="3bfce-135">태그</span><span class="sxs-lookup"><span data-stu-id="3bfce-135">-Tag</span></span>
<span data-ttu-id="3bfce-136">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="3bfce-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="3bfce-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3bfce-137">-Confirm</span></span>
<span data-ttu-id="3bfce-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bfce-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bfce-139">-WhatIf</span></span>
<span data-ttu-id="3bfce-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bfce-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bfce-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bfce-142">CommonParameters</span></span>
<span data-ttu-id="3bfce-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bfce-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3bfce-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bfce-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bfce-145">입력</span><span class="sxs-lookup"><span data-stu-id="3bfce-145">INPUTS</span></span>

### <span data-ttu-id="3bfce-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3bfce-146">System.String</span></span>

### <span data-ttu-id="3bfce-147">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3bfce-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="3bfce-148">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3bfce-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="3bfce-149">출력</span><span class="sxs-lookup"><span data-stu-id="3bfce-149">OUTPUTS</span></span>

### <span data-ttu-id="3bfce-150">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="3bfce-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="3bfce-151">상속자</span><span class="sxs-lookup"><span data-stu-id="3bfce-151">NOTES</span></span>

## <span data-ttu-id="3bfce-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bfce-152">RELATED LINKS</span></span>
