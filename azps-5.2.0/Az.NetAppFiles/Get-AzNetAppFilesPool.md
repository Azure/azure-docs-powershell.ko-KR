---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360067"
---
# <span data-ttu-id="f97a2-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f97a2-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="f97a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f97a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f97a2-103">ANF(Azure NetApp Files) 풀의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f97a2-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="f97a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f97a2-104">SYNTAX</span></span>

### <span data-ttu-id="f97a2-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f97a2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f97a2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f97a2-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f97a2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f97a2-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f97a2-108">설명</span><span class="sxs-lookup"><span data-stu-id="f97a2-108">DESCRIPTION</span></span>
<span data-ttu-id="f97a2-109">**Get-AzNetAppFilesPool** cmdlet은 ANF 풀의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f97a2-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="f97a2-110">예제</span><span class="sxs-lookup"><span data-stu-id="f97a2-110">EXAMPLES</span></span>

### <span data-ttu-id="f97a2-111">예제 1: ANF 풀을 얻게</span><span class="sxs-lookup"><span data-stu-id="f97a2-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="f97a2-112">이 명령은 "MyAnfAccount" 계정에서 MyAnfPool이라는 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f97a2-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="f97a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f97a2-113">PARAMETERS</span></span>

### <span data-ttu-id="f97a2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f97a2-114">-AccountName</span></span>
<span data-ttu-id="f97a2-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="f97a2-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="f97a2-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f97a2-116">-AccountObject</span></span>
<span data-ttu-id="f97a2-117">반환할 풀을 포함하는 계정 개체</span><span class="sxs-lookup"><span data-stu-id="f97a2-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="f97a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97a2-118">-DefaultProfile</span></span>
<span data-ttu-id="f97a2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f97a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f97a2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f97a2-120">-Name</span></span>
<span data-ttu-id="f97a2-121">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="f97a2-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f97a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f97a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f97a2-123">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="f97a2-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="f97a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f97a2-124">-ResourceId</span></span>
<span data-ttu-id="f97a2-125">ANF 풀의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f97a2-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="f97a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97a2-126">CommonParameters</span></span>
<span data-ttu-id="f97a2-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f97a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97a2-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f97a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97a2-129">입력</span><span class="sxs-lookup"><span data-stu-id="f97a2-129">INPUTS</span></span>

### <span data-ttu-id="f97a2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f97a2-130">System.String</span></span>

### <span data-ttu-id="f97a2-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f97a2-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f97a2-132">출력</span><span class="sxs-lookup"><span data-stu-id="f97a2-132">OUTPUTS</span></span>

### <span data-ttu-id="f97a2-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f97a2-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f97a2-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f97a2-134">NOTES</span></span>

## <span data-ttu-id="f97a2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f97a2-135">RELATED LINKS</span></span>
