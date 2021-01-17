---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339530"
---
# <span data-ttu-id="ffba1-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ffba1-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ffba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffba1-102">SYNOPSIS</span></span>
<span data-ttu-id="ffba1-103">지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ffba1-104">구문</span><span class="sxs-lookup"><span data-stu-id="ffba1-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffba1-105">설명</span><span class="sxs-lookup"><span data-stu-id="ffba1-105">DESCRIPTION</span></span>
<span data-ttu-id="ffba1-106">**Add-AzDataLakeStoreVirtualNetworkRule** cmdlet은 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ffba1-107">예제</span><span class="sxs-lookup"><span data-stu-id="ffba1-107">EXAMPLES</span></span>

### <span data-ttu-id="ffba1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffba1-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="ffba1-109">그러면 서브넷 ID "testId"가 있는 "dls" 계정에 "myVNET"이라는 새 가상 네트워크 규칙이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="ffba1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffba1-110">PARAMETERS</span></span>

### <span data-ttu-id="ffba1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ffba1-111">-Account</span></span>
<span data-ttu-id="ffba1-112">가상 네트워크 규칙을 추가할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="ffba1-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="ffba1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffba1-113">-DefaultProfile</span></span>
<span data-ttu-id="ffba1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffba1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ffba1-115">-Name</span></span>
<span data-ttu-id="ffba1-116">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffba1-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ffba1-117">-SubnetId</span></span>
<span data-ttu-id="ffba1-118">가상 네트워크 규칙의 subnetId</span><span class="sxs-lookup"><span data-stu-id="ffba1-118">The subnetId of the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffba1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffba1-119">-Confirm</span></span>
<span data-ttu-id="ffba1-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffba1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffba1-121">-WhatIf</span></span>
<span data-ttu-id="ffba1-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ffba1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffba1-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffba1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffba1-124">CommonParameters</span></span>
<span data-ttu-id="ffba1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ffba1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffba1-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ffba1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffba1-127">입력</span><span class="sxs-lookup"><span data-stu-id="ffba1-127">INPUTS</span></span>

### <span data-ttu-id="ffba1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ffba1-128">System.String</span></span>

## <span data-ttu-id="ffba1-129">출력</span><span class="sxs-lookup"><span data-stu-id="ffba1-129">OUTPUTS</span></span>

### <span data-ttu-id="ffba1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ffba1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ffba1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ffba1-131">NOTES</span></span>

## <span data-ttu-id="ffba1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffba1-132">RELATED LINKS</span></span>
