---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528524"
---
# <span data-ttu-id="e3857-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e3857-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e3857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3857-102">SYNOPSIS</span></span>
<span data-ttu-id="e3857-103">지정 된 Data Lake Store에서 지정 된 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e3857-104">가상 네트워크 규칙이 지정 되지 않은 경우 계정에 대 한 모든 가상 네트워크 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3857-105">구문과</span><span class="sxs-lookup"><span data-stu-id="e3857-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3857-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e3857-106">DESCRIPTION</span></span>
<span data-ttu-id="e3857-107">Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet은 지정 된 Data Lake Store에서 지정 된 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e3857-108">가상 네트워크 규칙이 지정 되지 않은 경우 계정에 대 한 모든 가상 네트워크 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e3857-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e3857-109">EXAMPLES</span></span>

### <span data-ttu-id="e3857-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3857-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="e3857-111">계정 "dl"에서 "myVNET" 이라는 가상 네트워크 규칙을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="e3857-112">변수</span><span class="sxs-lookup"><span data-stu-id="e3857-112">PARAMETERS</span></span>

### <span data-ttu-id="e3857-113">-계정</span><span class="sxs-lookup"><span data-stu-id="e3857-113">-Account</span></span>
<span data-ttu-id="e3857-114">가상 네트워크 규칙을 가져오는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="e3857-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="e3857-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3857-115">-DefaultProfile</span></span>
<span data-ttu-id="e3857-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3857-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e3857-117">-Name</span></span>
<span data-ttu-id="e3857-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e3857-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3857-119">CommonParameters</span></span>
<span data-ttu-id="e3857-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3857-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3857-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3857-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3857-122">입력</span><span class="sxs-lookup"><span data-stu-id="e3857-122">INPUTS</span></span>

### <span data-ttu-id="e3857-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3857-123">System.String</span></span>

## <span data-ttu-id="e3857-124">출력</span><span class="sxs-lookup"><span data-stu-id="e3857-124">OUTPUTS</span></span>

### <span data-ttu-id="e3857-125">DataLakeStore. DataLakeStoreVirtualNetworkRule/.</span><span class="sxs-lookup"><span data-stu-id="e3857-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e3857-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e3857-126">NOTES</span></span>

## <span data-ttu-id="e3857-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3857-127">RELATED LINKS</span></span>
