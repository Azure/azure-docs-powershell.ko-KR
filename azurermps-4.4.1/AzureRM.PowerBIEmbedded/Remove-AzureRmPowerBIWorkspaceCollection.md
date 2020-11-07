---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: c377beb022b3d44d8b96a560c4bdd8b0c6daa387
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711260"
---
# <span data-ttu-id="e0a80-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e0a80-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="e0a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a80-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a80-103">Power BI 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0a80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0a80-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0a80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0a80-105">DESCRIPTION</span></span>
<span data-ttu-id="e0a80-106">**AzureRmPowerBIWorkspaceCollection** Cmdlet은 Azure 구독 및 리소스 그룹에서 Power BI 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="e0a80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e0a80-107">EXAMPLES</span></span>

### <span data-ttu-id="e0a80-108">예제 1: 작업 영역 컬렉션 제거</span><span class="sxs-lookup"><span data-stu-id="e0a80-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="e0a80-109">이 명령은 지정 된 리소스 그룹에서 WCN11 이라는 작업 영역 컬렉션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="e0a80-110">변수</span><span class="sxs-lookup"><span data-stu-id="e0a80-110">PARAMETERS</span></span>

### <span data-ttu-id="e0a80-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a80-111">-ResourceGroupName</span></span>
<span data-ttu-id="e0a80-112">이 cmdlet이 작업 영역 컬렉션을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-112">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a80-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="e0a80-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="e0a80-114">이 cmdlet이 제거 하는 Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-114">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0a80-115">-확인</span><span class="sxs-lookup"><span data-stu-id="e0a80-115">-Confirm</span></span>
<span data-ttu-id="e0a80-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a80-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0a80-117">-WhatIf</span></span>
<span data-ttu-id="e0a80-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0a80-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0a80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a80-120">-DefaultProfile</span></span>
<span data-ttu-id="e0a80-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0a80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a80-122">CommonParameters</span></span>
<span data-ttu-id="e0a80-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a80-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0a80-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a80-125">입력</span><span class="sxs-lookup"><span data-stu-id="e0a80-125">INPUTS</span></span>

## <span data-ttu-id="e0a80-126">출력</span><span class="sxs-lookup"><span data-stu-id="e0a80-126">OUTPUTS</span></span>

## <span data-ttu-id="e0a80-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e0a80-127">NOTES</span></span>

## <span data-ttu-id="e0a80-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0a80-128">RELATED LINKS</span></span>

[<span data-ttu-id="e0a80-129">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e0a80-129">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="e0a80-130">새로운 AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="e0a80-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


