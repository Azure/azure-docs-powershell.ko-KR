---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704019"
---
# <span data-ttu-id="66c3d-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="66c3d-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="66c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="66c3d-103">Power BI 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66c3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66c3d-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="66c3d-106">**AzureRmPowerBIWorkspaceCollection** Cmdlet은 Azure 구독 및 리소스 그룹에서 Power BI 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="66c3d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="66c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="66c3d-108">예제 1: 작업 영역 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="66c3d-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="66c3d-109">이 명령은 지정 된 리소스 그룹에서 WCN11 이라는 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="66c3d-110">변수</span><span class="sxs-lookup"><span data-stu-id="66c3d-110">PARAMETERS</span></span>

### <span data-ttu-id="66c3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c3d-111">-DefaultProfile</span></span>
<span data-ttu-id="66c3d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="66c3d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c3d-113">-ResourceGroupName</span></span>
<span data-ttu-id="66c3d-114">이 cmdlet이 작업 영역 컬렉션을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="66c3d-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="66c3d-116">이 cmdlet이 제거 하는 Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="66c3d-117">-Confirm</span></span>
<span data-ttu-id="66c3d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c3d-119">-WhatIf</span></span>
<span data-ttu-id="66c3d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c3d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c3d-122">CommonParameters</span></span>
<span data-ttu-id="66c3d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c3d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c3d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c3d-125">입력</span><span class="sxs-lookup"><span data-stu-id="66c3d-125">INPUTS</span></span>

### <span data-ttu-id="66c3d-126">않아야</span><span class="sxs-lookup"><span data-stu-id="66c3d-126">None</span></span>
<span data-ttu-id="66c3d-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c3d-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66c3d-128">출력</span><span class="sxs-lookup"><span data-stu-id="66c3d-128">OUTPUTS</span></span>

## <span data-ttu-id="66c3d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="66c3d-129">NOTES</span></span>

## <span data-ttu-id="66c3d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66c3d-130">RELATED LINKS</span></span>

[<span data-ttu-id="66c3d-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="66c3d-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="66c3d-132">새로운 AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="66c3d-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


