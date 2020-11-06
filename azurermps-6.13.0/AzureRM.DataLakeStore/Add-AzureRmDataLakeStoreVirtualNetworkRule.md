---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: a25125b8aa76fa8d2be99f7f80b8fea2383bdf02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532027"
---
# <span data-ttu-id="66d9f-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="66d9f-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="66d9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="66d9f-103">지정 된 Data Lake Store 계정에 가상 네트워크 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66d9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66d9f-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66d9f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66d9f-105">DESCRIPTION</span></span>
<span data-ttu-id="66d9f-106">**추가-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet은 지정 된 Data Lake store 계정에 가상 네트워크 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-106">The **Add-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="66d9f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="66d9f-107">EXAMPLES</span></span>

### <span data-ttu-id="66d9f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="66d9f-108">Example 1</span></span>
```powershell
PS C:\> Add-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="66d9f-109">이렇게 하면 "testId" 계정 "dl"에 "myVNET" 이라는 새 가상 네트워크 규칙이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="66d9f-110">변수</span><span class="sxs-lookup"><span data-stu-id="66d9f-110">PARAMETERS</span></span>

### <span data-ttu-id="66d9f-111">-계정</span><span class="sxs-lookup"><span data-stu-id="66d9f-111">-Account</span></span>
<span data-ttu-id="66d9f-112">가상 네트워크 규칙을 추가할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="66d9f-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="66d9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d9f-113">-DefaultProfile</span></span>
<span data-ttu-id="66d9f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d9f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="66d9f-115">-Name</span></span>
<span data-ttu-id="66d9f-116">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="66d9f-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="66d9f-117">-SubnetId</span></span>
<span data-ttu-id="66d9f-118">가상 네트워크 규칙의 subnetId</span><span class="sxs-lookup"><span data-stu-id="66d9f-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="66d9f-119">-확인</span><span class="sxs-lookup"><span data-stu-id="66d9f-119">-Confirm</span></span>
<span data-ttu-id="66d9f-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66d9f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66d9f-121">-WhatIf</span></span>
<span data-ttu-id="66d9f-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66d9f-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66d9f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d9f-124">CommonParameters</span></span>
<span data-ttu-id="66d9f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66d9f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d9f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d9f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d9f-127">입력</span><span class="sxs-lookup"><span data-stu-id="66d9f-127">INPUTS</span></span>

### <span data-ttu-id="66d9f-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="66d9f-128">System.String</span></span>

## <span data-ttu-id="66d9f-129">출력</span><span class="sxs-lookup"><span data-stu-id="66d9f-129">OUTPUTS</span></span>

### <span data-ttu-id="66d9f-130">DataLakeStore. DataLakeStoreVirtualNetworkRule/.</span><span class="sxs-lookup"><span data-stu-id="66d9f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="66d9f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="66d9f-131">NOTES</span></span>

## <span data-ttu-id="66d9f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66d9f-132">RELATED LINKS</span></span>
