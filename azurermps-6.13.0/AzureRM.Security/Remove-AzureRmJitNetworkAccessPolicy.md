---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529386"
---
# <span data-ttu-id="36c1a-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36c1a-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="36c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="36c1a-103">JIT 네트워크 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36c1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36c1a-104">SYNTAX</span></span>

### <span data-ttu-id="36c1a-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="36c1a-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36c1a-106">리소스</span><span class="sxs-lookup"><span data-stu-id="36c1a-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36c1a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="36c1a-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36c1a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="36c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="36c1a-109">Just-in-time 네트워크 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="36c1a-110">이 작업을 수행한 후에는 사용자가 삭제 된 정책 내에서 구성 된 Vm에 대해 임시 네트워크 연결을 요청할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="36c1a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="36c1a-111">EXAMPLES</span></span>

### <span data-ttu-id="36c1a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="36c1a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="36c1a-113">Just-in-time 네트워크 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="36c1a-114">변수</span><span class="sxs-lookup"><span data-stu-id="36c1a-114">PARAMETERS</span></span>

### <span data-ttu-id="36c1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c1a-115">-DefaultProfile</span></span>
<span data-ttu-id="36c1a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36c1a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36c1a-117">-InputObject</span></span>
<span data-ttu-id="36c1a-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="36c1a-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-119">-위치</span><span class="sxs-lookup"><span data-stu-id="36c1a-119">-Location</span></span>
<span data-ttu-id="36c1a-120">Location.</span><span class="sxs-lookup"><span data-stu-id="36c1a-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="36c1a-121">-Name</span></span>
<span data-ttu-id="36c1a-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36c1a-123">-PassThru</span></span>
<span data-ttu-id="36c1a-124">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c1a-125">-ResourceGroupName</span></span>
<span data-ttu-id="36c1a-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36c1a-127">-ResourceId</span></span>
<span data-ttu-id="36c1a-128">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="36c1a-129">-Confirm</span></span>
<span data-ttu-id="36c1a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c1a-131">-WhatIf</span></span>
<span data-ttu-id="36c1a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36c1a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c1a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c1a-134">CommonParameters</span></span>
<span data-ttu-id="36c1a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36c1a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c1a-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c1a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c1a-137">입력</span><span class="sxs-lookup"><span data-stu-id="36c1a-137">INPUTS</span></span>

### <span data-ttu-id="36c1a-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36c1a-138">System.String</span></span>
<span data-ttu-id="36c1a-139">JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy에 대 한</span><span class="sxs-lookup"><span data-stu-id="36c1a-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="36c1a-140">출력</span><span class="sxs-lookup"><span data-stu-id="36c1a-140">OUTPUTS</span></span>

### <span data-ttu-id="36c1a-141">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="36c1a-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="36c1a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="36c1a-142">NOTES</span></span>

## <span data-ttu-id="36c1a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36c1a-143">RELATED LINKS</span></span>
