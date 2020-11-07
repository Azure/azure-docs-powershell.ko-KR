---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 56613276907772cfe3f2cbd99810ff247485913f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870954"
---
# <span data-ttu-id="43680-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="43680-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="43680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43680-102">SYNOPSIS</span></span>
<span data-ttu-id="43680-103">ANF (Azure NetApp Files) 풀의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43680-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="43680-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43680-104">SYNTAX</span></span>

### <span data-ttu-id="43680-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="43680-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43680-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43680-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43680-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43680-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43680-108">설명은</span><span class="sxs-lookup"><span data-stu-id="43680-108">DESCRIPTION</span></span>
<span data-ttu-id="43680-109">**Get-AzNetAppFilesPool** cmdlet은 anf 풀의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43680-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="43680-110">예제의</span><span class="sxs-lookup"><span data-stu-id="43680-110">EXAMPLES</span></span>

### <span data-ttu-id="43680-111">예제 1: ANF 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="43680-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="43680-112">이 명령은 "MyAnfAccount" 계정에서 MyAnfPool 이라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43680-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="43680-113">변수</span><span class="sxs-lookup"><span data-stu-id="43680-113">PARAMETERS</span></span>

### <span data-ttu-id="43680-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43680-114">-AccountName</span></span>
<span data-ttu-id="43680-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="43680-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="43680-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="43680-116">-AccountObject</span></span>
<span data-ttu-id="43680-117">반환할 풀이 포함 된 account 개체</span><span class="sxs-lookup"><span data-stu-id="43680-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="43680-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43680-118">-DefaultProfile</span></span>
<span data-ttu-id="43680-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43680-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43680-120">-이름</span><span class="sxs-lookup"><span data-stu-id="43680-120">-Name</span></span>
<span data-ttu-id="43680-121">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43680-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="43680-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43680-122">-ResourceGroupName</span></span>
<span data-ttu-id="43680-123">ANF 풀의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="43680-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="43680-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43680-124">-ResourceId</span></span>
<span data-ttu-id="43680-125">ANF 풀의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="43680-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="43680-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43680-126">CommonParameters</span></span>
<span data-ttu-id="43680-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43680-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="43680-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43680-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43680-129">입력</span><span class="sxs-lookup"><span data-stu-id="43680-129">INPUTS</span></span>

### <span data-ttu-id="43680-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43680-130">System.String</span></span>

### <span data-ttu-id="43680-131">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="43680-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="43680-132">출력</span><span class="sxs-lookup"><span data-stu-id="43680-132">OUTPUTS</span></span>

### <span data-ttu-id="43680-133">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="43680-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="43680-134">상속자</span><span class="sxs-lookup"><span data-stu-id="43680-134">NOTES</span></span>

## <span data-ttu-id="43680-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43680-135">RELATED LINKS</span></span>
