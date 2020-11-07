---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 68a9c47f3d5f5313a84729d0a7e0cdd5a2c3fac4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696743"
---
# <span data-ttu-id="eafd3-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="eafd3-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="eafd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eafd3-102">SYNOPSIS</span></span>
<span data-ttu-id="eafd3-103">DataShare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="eafd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eafd3-104">SYNTAX</span></span>

### <span data-ttu-id="eafd3-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eafd3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafd3-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="eafd3-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eafd3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eafd3-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafd3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eafd3-108">DESCRIPTION</span></span>
<span data-ttu-id="eafd3-109">**AzDataShareAccount** Cmdlet은 Azure 구독/리소스 그룹의 datashare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="eafd3-110">계정의 이름을 지정 하면이 cmdlet은 해당 datshare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="eafd3-111">이름을 지정 하지 않으면이 cmdlet은 Azure 구독/리소스 그룹의 모든 datashare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="eafd3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="eafd3-112">EXAMPLES</span></span>

### <span data-ttu-id="eafd3-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="eafd3-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="eafd3-114">이 명령은 Azure 구독에서 모든 datashare 계정에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="eafd3-115">변수</span><span class="sxs-lookup"><span data-stu-id="eafd3-115">PARAMETERS</span></span>

### <span data-ttu-id="eafd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafd3-116">-DefaultProfile</span></span>
<span data-ttu-id="eafd3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafd3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="eafd3-118">-Name</span></span>
<span data-ttu-id="eafd3-119">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafd3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafd3-120">-ResourceGroupName</span></span>
<span data-ttu-id="eafd3-121">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafd3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eafd3-122">-ResourceId</span></span>
<span data-ttu-id="eafd3-123">Azure data share 계정의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="eafd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafd3-124">CommonParameters</span></span>
<span data-ttu-id="eafd3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eafd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafd3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafd3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafd3-127">입력</span><span class="sxs-lookup"><span data-stu-id="eafd3-127">INPUTS</span></span>

### <span data-ttu-id="eafd3-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eafd3-128">System.String</span></span>

## <span data-ttu-id="eafd3-129">출력</span><span class="sxs-lookup"><span data-stu-id="eafd3-129">OUTPUTS</span></span>

### <span data-ttu-id="eafd3-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="eafd3-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="eafd3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="eafd3-131">NOTES</span></span>

## <span data-ttu-id="eafd3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eafd3-132">RELATED LINKS</span></span>