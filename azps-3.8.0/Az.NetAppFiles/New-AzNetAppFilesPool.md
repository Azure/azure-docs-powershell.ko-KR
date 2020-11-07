---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: 29fc27c16b8e084229134ed2389eab7685b1d43f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877292"
---
# <span data-ttu-id="f6a75-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f6a75-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="f6a75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6a75-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a75-103">새 Azure NetApp Files (ANF) 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="f6a75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6a75-104">SYNTAX</span></span>

### <span data-ttu-id="f6a75-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6a75-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6a75-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6a75-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6a75-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f6a75-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a75-108">**AzNetAppFilesPool** cmdlet은 anf 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="f6a75-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f6a75-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a75-110">예제 1: ANF 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="f6a75-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="f6a75-111">이 명령은 "MyAnfAccount" 계정 내에 새 ANF 풀 "MyAnfPool"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="f6a75-112">변수</span><span class="sxs-lookup"><span data-stu-id="f6a75-112">PARAMETERS</span></span>

### <span data-ttu-id="f6a75-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f6a75-113">-AccountName</span></span>
<span data-ttu-id="f6a75-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="f6a75-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f6a75-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f6a75-115">-AccountObject</span></span>
<span data-ttu-id="f6a75-116">새 풀 개체에 대 한 계정</span><span class="sxs-lookup"><span data-stu-id="f6a75-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="f6a75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a75-117">-DefaultProfile</span></span>
<span data-ttu-id="f6a75-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a75-119">-위치</span><span class="sxs-lookup"><span data-stu-id="f6a75-119">-Location</span></span>
<span data-ttu-id="f6a75-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="f6a75-120">The location of the resource</span></span>

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

### <span data-ttu-id="f6a75-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f6a75-121">-Name</span></span>
<span data-ttu-id="f6a75-122">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a75-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="f6a75-123">-PoolSize</span></span>
<span data-ttu-id="f6a75-124">ANF 풀의 크기</span><span class="sxs-lookup"><span data-stu-id="f6a75-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="f6a75-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a75-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6a75-126">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="f6a75-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f6a75-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f6a75-127">-ServiceLevel</span></span>
<span data-ttu-id="f6a75-128">ANF 풀의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="f6a75-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="f6a75-129">태그</span><span class="sxs-lookup"><span data-stu-id="f6a75-129">-Tag</span></span>
<span data-ttu-id="f6a75-130">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="f6a75-130">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f6a75-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f6a75-131">-Confirm</span></span>
<span data-ttu-id="f6a75-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6a75-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a75-133">-WhatIf</span></span>
<span data-ttu-id="f6a75-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a75-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6a75-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a75-136">CommonParameters</span></span>
<span data-ttu-id="f6a75-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6a75-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f6a75-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a75-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a75-139">입력</span><span class="sxs-lookup"><span data-stu-id="f6a75-139">INPUTS</span></span>

### <span data-ttu-id="f6a75-140">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f6a75-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f6a75-141">출력</span><span class="sxs-lookup"><span data-stu-id="f6a75-141">OUTPUTS</span></span>

### <span data-ttu-id="f6a75-142">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f6a75-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f6a75-143">상속자</span><span class="sxs-lookup"><span data-stu-id="f6a75-143">NOTES</span></span>

## <span data-ttu-id="f6a75-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6a75-144">RELATED LINKS</span></span>
