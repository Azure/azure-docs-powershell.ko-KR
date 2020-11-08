---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046084"
---
# <span data-ttu-id="92724-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="92724-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="92724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92724-102">SYNOPSIS</span></span>
<span data-ttu-id="92724-103">Azure RemoteApp 컬렉션에서 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="92724-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92724-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92724-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92724-105">DESCRIPTION</span></span>
<span data-ttu-id="92724-106">**AzureRemoteAppVM** cmdlet은 지정 된 사용자가 연결 된 Azure RemoteApp 컬렉션에서 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="92724-107">예제의</span><span class="sxs-lookup"><span data-stu-id="92724-107">EXAMPLES</span></span>

### <span data-ttu-id="92724-108">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="92724-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="92724-109">이 명령은 Contoso 라는 Azure RemoteApp 컬렉션에서 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="92724-110">사용자가 PattiFuller@contoso.com 이 가상 컴퓨터를 포함 하는 컬렉션에 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92724-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="92724-111">변수</span><span class="sxs-lookup"><span data-stu-id="92724-111">PARAMETERS</span></span>

### <span data-ttu-id="92724-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="92724-112">-CollectionName</span></span>
<span data-ttu-id="92724-113">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="92724-114">-LogoffMessage</span></span>
<span data-ttu-id="92724-115">이 cmdlet이 로그 오프 하기 전에 가상 컴퓨터에 연결 된 사용자에 게 표시 되는 경고 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="92724-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="92724-117">이 cmdlet이 사용자를 로그 아웃 하기 전에 대기 하는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="92724-118">기본값은 60 초입니다.</span><span class="sxs-lookup"><span data-stu-id="92724-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="92724-119">-Profile</span></span>
<span data-ttu-id="92724-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92724-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="92724-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92724-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="92724-122">-UserUpn</span></span>
<span data-ttu-id="92724-123">이 cmdlet이 가상 컴퓨터를 다시 시작 하는 사용자의 UPN (사용자 계정 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="92724-124">컬렉션 및 연결 된 Upn에서 가상 컴퓨터를 가져오려면 **AzureRemoteAppVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-125">-확인</span><span class="sxs-lookup"><span data-stu-id="92724-125">-Confirm</span></span>
<span data-ttu-id="92724-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92724-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92724-127">-WhatIf</span></span>
<span data-ttu-id="92724-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92724-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92724-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92724-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92724-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92724-130">CommonParameters</span></span>
<span data-ttu-id="92724-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92724-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92724-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92724-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92724-133">입력</span><span class="sxs-lookup"><span data-stu-id="92724-133">INPUTS</span></span>

## <span data-ttu-id="92724-134">출력</span><span class="sxs-lookup"><span data-stu-id="92724-134">OUTPUTS</span></span>

## <span data-ttu-id="92724-135">상속자</span><span class="sxs-lookup"><span data-stu-id="92724-135">NOTES</span></span>

## <span data-ttu-id="92724-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92724-136">RELATED LINKS</span></span>

[<span data-ttu-id="92724-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="92724-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


