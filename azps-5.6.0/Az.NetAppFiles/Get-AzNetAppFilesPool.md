---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 546364e96f7beed16ae8786dc3aaacbf9a84454d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968619"
---
# <span data-ttu-id="0d638-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0d638-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="0d638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d638-102">SYNOPSIS</span></span>
<span data-ttu-id="0d638-103">ANF(Azure NetApp Files) 풀에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0d638-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="0d638-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d638-104">SYNTAX</span></span>

### <span data-ttu-id="0d638-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0d638-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d638-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d638-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d638-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d638-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d638-108">설명</span><span class="sxs-lookup"><span data-stu-id="0d638-108">DESCRIPTION</span></span>
<span data-ttu-id="0d638-109">**Get-AzNetAppFilesPool** cmdlet은 ANF 풀에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0d638-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="0d638-110">예제</span><span class="sxs-lookup"><span data-stu-id="0d638-110">EXAMPLES</span></span>

### <span data-ttu-id="0d638-111">예제 1: ANF 풀을 얻다</span><span class="sxs-lookup"><span data-stu-id="0d638-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

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

<span data-ttu-id="0d638-112">이 명령은 계정 "MyAnfAccount"에서 MyAnfPool이라는 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0d638-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="0d638-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d638-113">PARAMETERS</span></span>

### <span data-ttu-id="0d638-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0d638-114">-AccountName</span></span>
<span data-ttu-id="0d638-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="0d638-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="0d638-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0d638-116">-AccountObject</span></span>
<span data-ttu-id="0d638-117">반환할 풀이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="0d638-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="0d638-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d638-118">-DefaultProfile</span></span>
<span data-ttu-id="0d638-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d638-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d638-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d638-120">-Name</span></span>
<span data-ttu-id="0d638-121">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="0d638-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d638-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d638-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d638-123">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="0d638-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="0d638-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d638-124">-ResourceId</span></span>
<span data-ttu-id="0d638-125">ANF 풀의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0d638-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="0d638-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d638-126">CommonParameters</span></span>
<span data-ttu-id="0d638-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d638-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d638-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d638-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d638-129">입력</span><span class="sxs-lookup"><span data-stu-id="0d638-129">INPUTS</span></span>

### <span data-ttu-id="0d638-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0d638-130">System.String</span></span>

### <span data-ttu-id="0d638-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0d638-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0d638-132">출력</span><span class="sxs-lookup"><span data-stu-id="0d638-132">OUTPUTS</span></span>

### <span data-ttu-id="0d638-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0d638-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="0d638-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d638-134">NOTES</span></span>

## <span data-ttu-id="0d638-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d638-135">RELATED LINKS</span></span>
