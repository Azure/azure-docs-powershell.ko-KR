---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056401"
---
# <span data-ttu-id="15edd-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="15edd-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="15edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15edd-102">SYNOPSIS</span></span>
<span data-ttu-id="15edd-103">DataShare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="15edd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15edd-104">SYNTAX</span></span>

### <span data-ttu-id="15edd-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="15edd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15edd-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="15edd-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15edd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15edd-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15edd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="15edd-108">DESCRIPTION</span></span>
<span data-ttu-id="15edd-109">**AzDataShareAccount** Cmdlet은 Azure 구독/리소스 그룹의 datashare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="15edd-110">계정의 이름을 지정 하면이 cmdlet은 해당 datshare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="15edd-111">이름을 지정 하지 않으면이 cmdlet은 Azure 구독/리소스 그룹의 모든 datashare 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="15edd-112">예제의</span><span class="sxs-lookup"><span data-stu-id="15edd-112">EXAMPLES</span></span>

### <span data-ttu-id="15edd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="15edd-113">Example 1</span></span>
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

<span data-ttu-id="15edd-114">이 명령은 Azure 구독에서 모든 datashare 계정에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="15edd-115">변수</span><span class="sxs-lookup"><span data-stu-id="15edd-115">PARAMETERS</span></span>

### <span data-ttu-id="15edd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15edd-116">-DefaultProfile</span></span>
<span data-ttu-id="15edd-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15edd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="15edd-118">-Name</span></span>
<span data-ttu-id="15edd-119">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="15edd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15edd-120">-ResourceGroupName</span></span>
<span data-ttu-id="15edd-121">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="15edd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15edd-122">-ResourceId</span></span>
<span data-ttu-id="15edd-123">Azure data share 계정의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="15edd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15edd-124">CommonParameters</span></span>
<span data-ttu-id="15edd-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15edd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15edd-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15edd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15edd-127">입력</span><span class="sxs-lookup"><span data-stu-id="15edd-127">INPUTS</span></span>

### <span data-ttu-id="15edd-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15edd-128">System.String</span></span>

## <span data-ttu-id="15edd-129">출력</span><span class="sxs-lookup"><span data-stu-id="15edd-129">OUTPUTS</span></span>

### <span data-ttu-id="15edd-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="15edd-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="15edd-131">상속자</span><span class="sxs-lookup"><span data-stu-id="15edd-131">NOTES</span></span>

## <span data-ttu-id="15edd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15edd-132">RELATED LINKS</span></span>
