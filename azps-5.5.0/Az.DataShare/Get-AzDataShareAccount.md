---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186116"
---
# <span data-ttu-id="130b5-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="130b5-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="130b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="130b5-102">SYNOPSIS</span></span>
<span data-ttu-id="130b5-103">DataShare 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="130b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="130b5-104">SYNTAX</span></span>

### <span data-ttu-id="130b5-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="130b5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="130b5-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="130b5-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="130b5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="130b5-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="130b5-108">설명</span><span class="sxs-lookup"><span data-stu-id="130b5-108">DESCRIPTION</span></span>
<span data-ttu-id="130b5-109">**Get-AzDataShareAccount** cmdlet은 Azure 구독/리소스 그룹의 데이터 공유 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="130b5-110">계정 이름을 지정하면 이 cmdlet은 해당 datshare 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="130b5-111">이름을 지정하지 않으면 이 cmdlet은 Azure 구독/리소스 그룹의 모든 데이터 공유 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="130b5-112">예제</span><span class="sxs-lookup"><span data-stu-id="130b5-112">EXAMPLES</span></span>

### <span data-ttu-id="130b5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="130b5-113">Example 1</span></span>
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

<span data-ttu-id="130b5-114">이 명령은 Azure 구독의 모든 데이터 공유 계정에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="130b5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="130b5-115">PARAMETERS</span></span>

### <span data-ttu-id="130b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="130b5-116">-DefaultProfile</span></span>
<span data-ttu-id="130b5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="130b5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="130b5-118">-Name</span></span>
<span data-ttu-id="130b5-119">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="130b5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="130b5-120">-ResourceGroupName</span></span>
<span data-ttu-id="130b5-121">Azure 데이터 공유 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="130b5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="130b5-122">-ResourceId</span></span>
<span data-ttu-id="130b5-123">Azure 데이터 공유 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="130b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130b5-124">CommonParameters</span></span>
<span data-ttu-id="130b5-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="130b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130b5-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="130b5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130b5-127">입력</span><span class="sxs-lookup"><span data-stu-id="130b5-127">INPUTS</span></span>

### <span data-ttu-id="130b5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="130b5-128">System.String</span></span>

## <span data-ttu-id="130b5-129">출력</span><span class="sxs-lookup"><span data-stu-id="130b5-129">OUTPUTS</span></span>

### <span data-ttu-id="130b5-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="130b5-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="130b5-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="130b5-131">NOTES</span></span>

## <span data-ttu-id="130b5-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="130b5-132">RELATED LINKS</span></span>
