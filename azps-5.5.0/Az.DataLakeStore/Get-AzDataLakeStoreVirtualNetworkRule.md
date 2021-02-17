---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194657"
---
# <span data-ttu-id="669d7-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="669d7-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="669d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669d7-102">SYNOPSIS</span></span>
<span data-ttu-id="669d7-103">지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="669d7-104">가상 네트워크 규칙을 지정하지 않으면 계정에 대한 모든 가상 네트워크 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="669d7-105">구문</span><span class="sxs-lookup"><span data-stu-id="669d7-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="669d7-106">설명</span><span class="sxs-lookup"><span data-stu-id="669d7-106">DESCRIPTION</span></span>
<span data-ttu-id="669d7-107">Get-AzDataLakeStoreVirtualNetworkRule cmdlet은 지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="669d7-108">가상 네트워크 규칙을 지정하지 않으면 계정에 대한 모든 가상 네트워크 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="669d7-109">예제</span><span class="sxs-lookup"><span data-stu-id="669d7-109">EXAMPLES</span></span>

### <span data-ttu-id="669d7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="669d7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="669d7-111">계정 "dls"에서 "myVNET"이라는 가상 네트워크 규칙을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="669d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="669d7-112">PARAMETERS</span></span>

### <span data-ttu-id="669d7-113">-Account</span><span class="sxs-lookup"><span data-stu-id="669d7-113">-Account</span></span>
<span data-ttu-id="669d7-114">가상 네트워크 규칙을 얻을 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="669d7-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="669d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669d7-115">-DefaultProfile</span></span>
<span data-ttu-id="669d7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="669d7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="669d7-117">-Name</span></span>
<span data-ttu-id="669d7-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="669d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669d7-119">CommonParameters</span></span>
<span data-ttu-id="669d7-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="669d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669d7-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="669d7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669d7-122">입력</span><span class="sxs-lookup"><span data-stu-id="669d7-122">INPUTS</span></span>

### <span data-ttu-id="669d7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="669d7-123">System.String</span></span>

## <span data-ttu-id="669d7-124">출력</span><span class="sxs-lookup"><span data-stu-id="669d7-124">OUTPUTS</span></span>

### <span data-ttu-id="669d7-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="669d7-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="669d7-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="669d7-126">NOTES</span></span>

## <span data-ttu-id="669d7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="669d7-127">RELATED LINKS</span></span>
