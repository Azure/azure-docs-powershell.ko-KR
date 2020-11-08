---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042326"
---
# <span data-ttu-id="be88c-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="be88c-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="be88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be88c-102">SYNOPSIS</span></span>
<span data-ttu-id="be88c-103">지정 된 선택 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-103">Resets the specified access key.</span></span>

## <span data-ttu-id="be88c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be88c-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be88c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be88c-105">DESCRIPTION</span></span>
<span data-ttu-id="be88c-106">**AzPowerBIWorkspaceCollectionAccessKey** Cmdlet은 Power BI workspace 컬렉션에서 지정 된 선택 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="be88c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be88c-107">EXAMPLES</span></span>

### <span data-ttu-id="be88c-108">예제 1: 기본 선택 키 다시 설정</span><span class="sxs-lookup"><span data-stu-id="be88c-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="be88c-109">이 명령은 지정 된 리소스 그룹의 WCN11 이라는 작업 영역 컬렉션에 대 한 기본 선택 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="be88c-110">변수</span><span class="sxs-lookup"><span data-stu-id="be88c-110">PARAMETERS</span></span>

### <span data-ttu-id="be88c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be88c-111">-DefaultProfile</span></span>
<span data-ttu-id="be88c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="be88c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be88c-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="be88c-113">-Key1</span></span>
<span data-ttu-id="be88c-114">이 cmdlet이 기본 선택 키를 다시 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-114">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be88c-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="be88c-115">-Key2</span></span>
<span data-ttu-id="be88c-116">이 cmdlet이 보조 선택 키를 다시 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-116">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be88c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be88c-117">-ResourceGroupName</span></span>
<span data-ttu-id="be88c-118">컬렉션의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="be88c-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="be88c-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="be88c-120">이 cmdlet이 작동 하는 Power BI 작업 영역 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="be88c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="be88c-121">-Confirm</span></span>
<span data-ttu-id="be88c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be88c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be88c-123">-WhatIf</span></span>
<span data-ttu-id="be88c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be88c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be88c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be88c-126">CommonParameters</span></span>
<span data-ttu-id="be88c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be88c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be88c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be88c-129">입력</span><span class="sxs-lookup"><span data-stu-id="be88c-129">INPUTS</span></span>

### <span data-ttu-id="be88c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be88c-130">System.String</span></span>

## <span data-ttu-id="be88c-131">출력</span><span class="sxs-lookup"><span data-stu-id="be88c-131">OUTPUTS</span></span>

### <span data-ttu-id="be88c-132">PSWorkspaceCollectionAccessKey. PowerBIEmbedded. \*.</span><span class="sxs-lookup"><span data-stu-id="be88c-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="be88c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="be88c-133">NOTES</span></span>

## <span data-ttu-id="be88c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be88c-134">RELATED LINKS</span></span>

[<span data-ttu-id="be88c-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="be88c-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


