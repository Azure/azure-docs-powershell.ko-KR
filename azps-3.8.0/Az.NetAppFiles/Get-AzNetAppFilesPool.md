---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 613f9b2703dcdf16a6f4d87dd1cdc4c8938c1bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877298"
---
# <span data-ttu-id="cd62b-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="cd62b-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="cd62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd62b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd62b-103">ANF (Azure NetApp Files) 풀의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd62b-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="cd62b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd62b-104">SYNTAX</span></span>

### <span data-ttu-id="cd62b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd62b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd62b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd62b-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd62b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd62b-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd62b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cd62b-108">DESCRIPTION</span></span>
<span data-ttu-id="cd62b-109">**Get-AzNetAppFilesPool** cmdlet은 anf 풀의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd62b-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="cd62b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cd62b-110">EXAMPLES</span></span>

### <span data-ttu-id="cd62b-111">예제 1: ANF 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd62b-111">Example 1: Get an ANF pool</span></span>
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
ProvisioningState : Succeeded
```

<span data-ttu-id="cd62b-112">이 명령은 "MyAnfAccount" 계정에서 MyAnfPool 이라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd62b-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="cd62b-113">변수</span><span class="sxs-lookup"><span data-stu-id="cd62b-113">PARAMETERS</span></span>

### <span data-ttu-id="cd62b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd62b-114">-AccountName</span></span>
<span data-ttu-id="cd62b-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="cd62b-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="cd62b-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="cd62b-116">-AccountObject</span></span>
<span data-ttu-id="cd62b-117">반환할 풀이 포함 된 account 개체</span><span class="sxs-lookup"><span data-stu-id="cd62b-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="cd62b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd62b-118">-DefaultProfile</span></span>
<span data-ttu-id="cd62b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd62b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd62b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="cd62b-120">-Name</span></span>
<span data-ttu-id="cd62b-121">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd62b-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd62b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd62b-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd62b-123">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="cd62b-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="cd62b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd62b-124">-ResourceId</span></span>
<span data-ttu-id="cd62b-125">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="cd62b-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="cd62b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd62b-126">CommonParameters</span></span>
<span data-ttu-id="cd62b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd62b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd62b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd62b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd62b-129">입력</span><span class="sxs-lookup"><span data-stu-id="cd62b-129">INPUTS</span></span>

### <span data-ttu-id="cd62b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd62b-130">System.String</span></span>

### <span data-ttu-id="cd62b-131">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cd62b-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="cd62b-132">출력</span><span class="sxs-lookup"><span data-stu-id="cd62b-132">OUTPUTS</span></span>

### <span data-ttu-id="cd62b-133">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="cd62b-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="cd62b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="cd62b-134">NOTES</span></span>

## <span data-ttu-id="cd62b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd62b-135">RELATED LINKS</span></span>
