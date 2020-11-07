---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 981daec060f47a88b31454cd8d13711091bedcf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536260"
---
# <span data-ttu-id="0ed8c-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0ed8c-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0ed8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed8c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed8c-103">Power BI 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ed8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ed8c-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ed8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ed8c-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed8c-106">**AzureRmPowerBIWorkspaceCollection** cmdlet은 지정 된 리소스 그룹 및 위치에서 Azure 구독에 대 한 Power BI 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="0ed8c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ed8c-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed8c-108">예제 1: 작업 영역 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="0ed8c-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="0ed8c-109">이 명령은 지정 된 위치에 지정 된 리소스 그룹에 WCN11 이라는 작업 영역 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="0ed8c-110">변수</span><span class="sxs-lookup"><span data-stu-id="0ed8c-110">PARAMETERS</span></span>

### <span data-ttu-id="0ed8c-111">-위치</span><span class="sxs-lookup"><span data-stu-id="0ed8c-111">-Location</span></span>
<span data-ttu-id="0ed8c-112">이 cmdlet이 작업 영역 컬렉션을 만드는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-112">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="0ed8c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed8c-113">-ResourceGroupName</span></span>
<span data-ttu-id="0ed8c-114">이 cmdlet이 작업 영역 컬렉션을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-114">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="0ed8c-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0ed8c-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0ed8c-116">Power BI workspace 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-116">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="0ed8c-117">-확인</span><span class="sxs-lookup"><span data-stu-id="0ed8c-117">-Confirm</span></span>
<span data-ttu-id="0ed8c-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed8c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed8c-119">-WhatIf</span></span>
<span data-ttu-id="0ed8c-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ed8c-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed8c-122">-DefaultProfile</span></span>
<span data-ttu-id="0ed8c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed8c-124">CommonParameters</span></span>
<span data-ttu-id="0ed8c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed8c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed8c-127">입력</span><span class="sxs-lookup"><span data-stu-id="0ed8c-127">INPUTS</span></span>

## <span data-ttu-id="0ed8c-128">출력</span><span class="sxs-lookup"><span data-stu-id="0ed8c-128">OUTPUTS</span></span>

### <span data-ttu-id="0ed8c-129">PSWorkspaceCollection. PowerBIEmbedded. \*.</span><span class="sxs-lookup"><span data-stu-id="0ed8c-129">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="0ed8c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0ed8c-130">NOTES</span></span>

## <span data-ttu-id="0ed8c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ed8c-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ed8c-132">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0ed8c-132">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0ed8c-133">제거-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0ed8c-133">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)

