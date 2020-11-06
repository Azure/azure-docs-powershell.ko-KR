---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537383"
---
# <span data-ttu-id="bff15-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="bff15-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="bff15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff15-102">SYNOPSIS</span></span>
<span data-ttu-id="bff15-103">디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bff15-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff15-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bff15-105">DESCRIPTION</span></span>
<span data-ttu-id="bff15-106">**AzureRmDisk** cmdlet이 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="bff15-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bff15-107">EXAMPLES</span></span>

### <span data-ttu-id="bff15-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bff15-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="bff15-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Disk01 ' 인 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bff15-110">변수</span><span class="sxs-lookup"><span data-stu-id="bff15-110">PARAMETERS</span></span>

### <span data-ttu-id="bff15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff15-111">-DefaultProfile</span></span>
<span data-ttu-id="bff15-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff15-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="bff15-113">-DiskName</span></span>
<span data-ttu-id="bff15-114">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff15-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bff15-115">-Force</span></span>
<span data-ttu-id="bff15-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bff15-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff15-117">-ResourceGroupName</span></span>
<span data-ttu-id="bff15-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bff15-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bff15-119">-Confirm</span></span>
<span data-ttu-id="bff15-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff15-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff15-121">-WhatIf</span></span>
<span data-ttu-id="bff15-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff15-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff15-124">CommonParameters</span></span>
<span data-ttu-id="bff15-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bff15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff15-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff15-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff15-127">입력</span><span class="sxs-lookup"><span data-stu-id="bff15-127">INPUTS</span></span>

### <span data-ttu-id="bff15-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bff15-128">System.String</span></span>

## <span data-ttu-id="bff15-129">출력</span><span class="sxs-lookup"><span data-stu-id="bff15-129">OUTPUTS</span></span>

### <span data-ttu-id="bff15-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="bff15-130">System.Object</span></span>

## <span data-ttu-id="bff15-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bff15-131">NOTES</span></span>

## <span data-ttu-id="bff15-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bff15-132">RELATED LINKS</span></span>

