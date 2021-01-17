---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345477"
---
# <span data-ttu-id="dfce9-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dfce9-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="dfce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfce9-102">SYNOPSIS</span></span>
<span data-ttu-id="dfce9-103">지정된 액세스 키를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-103">Resets the specified access key.</span></span>

## <span data-ttu-id="dfce9-104">구문</span><span class="sxs-lookup"><span data-stu-id="dfce9-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfce9-105">설명</span><span class="sxs-lookup"><span data-stu-id="dfce9-105">DESCRIPTION</span></span>
<span data-ttu-id="dfce9-106">**Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet은 Power BI 작업 영역 컬렉션에서 지정된 액세스 키를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="dfce9-107">예제</span><span class="sxs-lookup"><span data-stu-id="dfce9-107">EXAMPLES</span></span>

### <span data-ttu-id="dfce9-108">예제 1: 기본 액세스 키 다시 설정</span><span class="sxs-lookup"><span data-stu-id="dfce9-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="dfce9-109">이 명령은 지정된 리소스 그룹에서 WCN11이라는 작업 영역 컬렉션에 대한 기본 액세스 키를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="dfce9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfce9-110">PARAMETERS</span></span>

### <span data-ttu-id="dfce9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfce9-111">-DefaultProfile</span></span>
<span data-ttu-id="dfce9-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dfce9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfce9-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="dfce9-113">-Key1</span></span>
<span data-ttu-id="dfce9-114">이 cmdlet이 기본 액세스 키를 다시 설정하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="dfce9-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="dfce9-115">-Key2</span></span>
<span data-ttu-id="dfce9-116">이 cmdlet이 보조 액세스 키를 다시 설정하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="dfce9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfce9-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfce9-118">컬렉션의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="dfce9-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="dfce9-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="dfce9-120">이 cmdlet이 작동하는 Power BI 작업 영역 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dfce9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfce9-121">-Confirm</span></span>
<span data-ttu-id="dfce9-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfce9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfce9-123">-WhatIf</span></span>
<span data-ttu-id="dfce9-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dfce9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfce9-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfce9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfce9-126">CommonParameters</span></span>
<span data-ttu-id="dfce9-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfce9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfce9-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dfce9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfce9-129">입력</span><span class="sxs-lookup"><span data-stu-id="dfce9-129">INPUTS</span></span>

### <span data-ttu-id="dfce9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dfce9-130">System.String</span></span>

## <span data-ttu-id="dfce9-131">출력</span><span class="sxs-lookup"><span data-stu-id="dfce9-131">OUTPUTS</span></span>

### <span data-ttu-id="dfce9-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dfce9-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="dfce9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dfce9-133">NOTES</span></span>

## <span data-ttu-id="dfce9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfce9-134">RELATED LINKS</span></span>

[<span data-ttu-id="dfce9-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dfce9-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


