---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305468"
---
# <span data-ttu-id="b5ddc-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b5ddc-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b5ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ddc-103">지정 된 Data Lake Store에서 지정 된 가상 네트워크 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b5ddc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5ddc-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ddc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ddc-106">**AzDataLakeStoreVirtualNetworkRule** cmdlet은 지정 된 Data Lake store에서 지정 된 가상 네트워크 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b5ddc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5ddc-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ddc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5ddc-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b5ddc-109">"Dl" 계정에 있는 가상 네트워크 규칙 "myVNET"의 서브넷 id를 "updatedId"로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="b5ddc-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5ddc-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ddc-111">-계정</span><span class="sxs-lookup"><span data-stu-id="b5ddc-111">-Account</span></span>
<span data-ttu-id="b5ddc-112">의 가상 네트워크 규칙을 업데이트 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="b5ddc-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="b5ddc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ddc-113">-DefaultProfile</span></span>
<span data-ttu-id="b5ddc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ddc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b5ddc-115">-Name</span></span>
<span data-ttu-id="b5ddc-116">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b5ddc-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b5ddc-117">-SubnetId</span></span>
<span data-ttu-id="b5ddc-118">가상 네트워크 규칙에 대 한 유효한 ip 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="b5ddc-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="b5ddc-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b5ddc-119">-Confirm</span></span>
<span data-ttu-id="b5ddc-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ddc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ddc-121">-WhatIf</span></span>
<span data-ttu-id="b5ddc-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ddc-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ddc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ddc-124">CommonParameters</span></span>
<span data-ttu-id="b5ddc-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ddc-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ddc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ddc-127">입력</span><span class="sxs-lookup"><span data-stu-id="b5ddc-127">INPUTS</span></span>

### <span data-ttu-id="b5ddc-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b5ddc-128">System.String</span></span>

## <span data-ttu-id="b5ddc-129">출력</span><span class="sxs-lookup"><span data-stu-id="b5ddc-129">OUTPUTS</span></span>

### <span data-ttu-id="b5ddc-130">DataLakeStore. DataLakeStoreVirtualNetworkRule/.</span><span class="sxs-lookup"><span data-stu-id="b5ddc-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b5ddc-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b5ddc-131">NOTES</span></span>

## <span data-ttu-id="b5ddc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5ddc-132">RELATED LINKS</span></span>
