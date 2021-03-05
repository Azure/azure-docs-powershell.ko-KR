---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 98f4dd2a1076df1954674f67829e3ee14da1d871
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995582"
---
# <span data-ttu-id="128a1-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="128a1-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="128a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="128a1-102">SYNOPSIS</span></span>
<span data-ttu-id="128a1-103">지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="128a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="128a1-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="128a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="128a1-105">DESCRIPTION</span></span>
<span data-ttu-id="128a1-106">**Set-AzDataLakeStoreVirtualNetworkRule** cmdlet은 지정된 Data Lake Store에서 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="128a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="128a1-107">EXAMPLES</span></span>

### <span data-ttu-id="128a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="128a1-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="128a1-109">계정 "dls"에서 가상 네트워크 규칙 "myVNET"의 서브넷 ID를 "updatedId"로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="128a1-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="128a1-110">PARAMETERS</span></span>

### <span data-ttu-id="128a1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="128a1-111">-Account</span></span>
<span data-ttu-id="128a1-112">에서 가상 네트워크 규칙을 업데이트하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="128a1-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="128a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128a1-113">-DefaultProfile</span></span>
<span data-ttu-id="128a1-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128a1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="128a1-115">-Name</span></span>
<span data-ttu-id="128a1-116">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="128a1-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="128a1-117">-SubnetId</span></span>
<span data-ttu-id="128a1-118">가상 네트워크 규칙에 대한 유효한 IP 범위 시작</span><span class="sxs-lookup"><span data-stu-id="128a1-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="128a1-119">-확인</span><span class="sxs-lookup"><span data-stu-id="128a1-119">-Confirm</span></span>
<span data-ttu-id="128a1-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="128a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="128a1-121">-WhatIf</span></span>
<span data-ttu-id="128a1-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="128a1-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="128a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128a1-124">CommonParameters</span></span>
<span data-ttu-id="128a1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="128a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128a1-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="128a1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128a1-127">입력</span><span class="sxs-lookup"><span data-stu-id="128a1-127">INPUTS</span></span>

### <span data-ttu-id="128a1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="128a1-128">System.String</span></span>

## <span data-ttu-id="128a1-129">출력</span><span class="sxs-lookup"><span data-stu-id="128a1-129">OUTPUTS</span></span>

### <span data-ttu-id="128a1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="128a1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="128a1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="128a1-131">NOTES</span></span>

## <span data-ttu-id="128a1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="128a1-132">RELATED LINKS</span></span>
