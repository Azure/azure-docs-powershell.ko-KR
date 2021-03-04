---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977136"
---
# <span data-ttu-id="3777b-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3777b-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3777b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3777b-102">SYNOPSIS</span></span>
<span data-ttu-id="3777b-103">지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="3777b-104">가상 네트워크 규칙이 지정되지 않은 경우 계정에 대한 모든 가상 네트워크 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="3777b-105">구문</span><span class="sxs-lookup"><span data-stu-id="3777b-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3777b-106">설명</span><span class="sxs-lookup"><span data-stu-id="3777b-106">DESCRIPTION</span></span>
<span data-ttu-id="3777b-107">Get-AzDataLakeStoreVirtualNetworkRule cmdlet은 지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="3777b-108">가상 네트워크 규칙이 지정되지 않은 경우 계정에 대한 모든 가상 네트워크 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="3777b-109">예제</span><span class="sxs-lookup"><span data-stu-id="3777b-109">EXAMPLES</span></span>

### <span data-ttu-id="3777b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3777b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="3777b-111">계정 "dls"에서 "myVNET"이라는 가상 네트워크 규칙을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="3777b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3777b-112">PARAMETERS</span></span>

### <span data-ttu-id="3777b-113">-Account</span><span class="sxs-lookup"><span data-stu-id="3777b-113">-Account</span></span>
<span data-ttu-id="3777b-114">가상 네트워크 규칙을 얻을 수 있는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="3777b-114">The Data Lake Store account to get the virtual network rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3777b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3777b-115">-DefaultProfile</span></span>
<span data-ttu-id="3777b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3777b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3777b-117">-Name</span></span>
<span data-ttu-id="3777b-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3777b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3777b-119">CommonParameters</span></span>
<span data-ttu-id="3777b-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3777b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3777b-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3777b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3777b-122">입력</span><span class="sxs-lookup"><span data-stu-id="3777b-122">INPUTS</span></span>

### <span data-ttu-id="3777b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3777b-123">System.String</span></span>

## <span data-ttu-id="3777b-124">출력</span><span class="sxs-lookup"><span data-stu-id="3777b-124">OUTPUTS</span></span>

### <span data-ttu-id="3777b-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3777b-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3777b-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3777b-126">NOTES</span></span>

## <span data-ttu-id="3777b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3777b-127">RELATED LINKS</span></span>
