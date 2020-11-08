---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056515"
---
# <span data-ttu-id="99e54-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="99e54-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="99e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e54-102">SYNOPSIS</span></span>
<span data-ttu-id="99e54-103">디스크 암호화 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="99e54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99e54-104">SYNTAX</span></span>

### <span data-ttu-id="99e54-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="99e54-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e54-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="99e54-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e54-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="99e54-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99e54-108">설명은</span><span class="sxs-lookup"><span data-stu-id="99e54-108">DESCRIPTION</span></span>
<span data-ttu-id="99e54-109">디스크 암호화 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="99e54-110">예제의</span><span class="sxs-lookup"><span data-stu-id="99e54-110">EXAMPLES</span></span>

### <span data-ttu-id="99e54-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="99e54-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="99e54-112">' Rg1 '의 ' enc1 ' 디스크 암호화 집합 삭제</span><span class="sxs-lookup"><span data-stu-id="99e54-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="99e54-113">변수</span><span class="sxs-lookup"><span data-stu-id="99e54-113">PARAMETERS</span></span>

### <span data-ttu-id="99e54-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99e54-114">-AsJob</span></span>
<span data-ttu-id="99e54-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="99e54-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99e54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e54-116">-DefaultProfile</span></span>
<span data-ttu-id="99e54-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e54-118">-Force</span><span class="sxs-lookup"><span data-stu-id="99e54-118">-Force</span></span>
<span data-ttu-id="99e54-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99e54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99e54-120">-InputObject</span></span>
<span data-ttu-id="99e54-121">디스크 암호화 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e54-122">-이름</span><span class="sxs-lookup"><span data-stu-id="99e54-122">-Name</span></span>
<span data-ttu-id="99e54-123">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e54-124">-ResourceGroupName</span></span>
<span data-ttu-id="99e54-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e54-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99e54-126">-ResourceId</span></span>
<span data-ttu-id="99e54-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e54-128">-확인</span><span class="sxs-lookup"><span data-stu-id="99e54-128">-Confirm</span></span>
<span data-ttu-id="99e54-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e54-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e54-130">-WhatIf</span></span>
<span data-ttu-id="99e54-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e54-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e54-133">CommonParameters</span></span>
<span data-ttu-id="99e54-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e54-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99e54-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e54-136">입력</span><span class="sxs-lookup"><span data-stu-id="99e54-136">INPUTS</span></span>

### <span data-ttu-id="99e54-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99e54-137">System.String</span></span>

### <span data-ttu-id="99e54-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="99e54-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="99e54-139">출력</span><span class="sxs-lookup"><span data-stu-id="99e54-139">OUTPUTS</span></span>

### <span data-ttu-id="99e54-140">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="99e54-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="99e54-141">상속자</span><span class="sxs-lookup"><span data-stu-id="99e54-141">NOTES</span></span>

## <span data-ttu-id="99e54-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99e54-142">RELATED LINKS</span></span>
