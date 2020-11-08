---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045952"
---
# <span data-ttu-id="d6cda-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="d6cda-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="d6cda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6cda-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cda-103">역할의 인스턴스 수 또는 런타임 버전을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="d6cda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6cda-104">SYNTAX</span></span>

### <span data-ttu-id="d6cda-105">모두</span><span class="sxs-lookup"><span data-stu-id="d6cda-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6cda-106">런타임</span><span class="sxs-lookup"><span data-stu-id="d6cda-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d6cda-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="d6cda-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6cda-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d6cda-108">DESCRIPTION</span></span>
<span data-ttu-id="d6cda-109">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d6cda-110">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d6cda-111">**Set-AzureServiceProjectRole** cmdlet은 지정 된 역할에 대 한 역할 인스턴스의 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="d6cda-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d6cda-112">EXAMPLES</span></span>

### <span data-ttu-id="d6cda-113">예제 1: 웹 역할의 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="d6cda-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="d6cda-114">MyWebRole1 이라는 웹 역할의 인스턴스 수를 2로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="d6cda-115">예제 2: 작업자 역할의 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="d6cda-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="d6cda-116">WorkerRole1 이라는 작업자 역할의 역할 인스턴스 수를 2로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="d6cda-117">예제 3: 역할 서비스에 대 한 런타임 버전 설정</span><span class="sxs-lookup"><span data-stu-id="d6cda-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="d6cda-118">역할 MyRole1에 대 한 node.exe 런타임 버전을 0.6.20로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="d6cda-119">변수</span><span class="sxs-lookup"><span data-stu-id="d6cda-119">PARAMETERS</span></span>

### <span data-ttu-id="d6cda-120">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="d6cda-120">-Instances</span></span>
<span data-ttu-id="d6cda-121">지정 된 웹 또는 작업자 역할에 대 한 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cda-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6cda-122">-PassThru</span></span>
<span data-ttu-id="d6cda-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6cda-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6cda-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="d6cda-125">-Profile</span></span>
<span data-ttu-id="d6cda-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6cda-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cda-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="d6cda-128">-RoleName</span></span>
<span data-ttu-id="d6cda-129">변경할 웹 또는 작업자 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-129">Specifies the name of the web or worker role to be changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cda-130">런타임</span><span class="sxs-lookup"><span data-stu-id="d6cda-130">-Runtime</span></span>
<span data-ttu-id="d6cda-131">지정 된 역할에 추가할 런타임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cda-132">-버전</span><span class="sxs-lookup"><span data-stu-id="d6cda-132">-Version</span></span>
<span data-ttu-id="d6cda-133">역할에 추가할 런타임 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cda-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="d6cda-134">-VMSize</span></span>
<span data-ttu-id="d6cda-135">역할의 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cda-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cda-136">CommonParameters</span></span>
<span data-ttu-id="d6cda-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cda-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6cda-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cda-139">입력</span><span class="sxs-lookup"><span data-stu-id="d6cda-139">INPUTS</span></span>

###  
<span data-ttu-id="d6cda-140">가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cda-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="d6cda-141">출력</span><span class="sxs-lookup"><span data-stu-id="d6cda-141">OUTPUTS</span></span>

## <span data-ttu-id="d6cda-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d6cda-142">NOTES</span></span>

## <span data-ttu-id="d6cda-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6cda-143">RELATED LINKS</span></span>

[<span data-ttu-id="d6cda-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d6cda-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


